---
name: sync
description: Figma 디자인 시스템이 수정됐을 때 design-system/ 문서(tokens 4종 + components 전체 + index)를 한 번에 최신화한다. "디자인 시스템 동기화", "figma 재덤프해서 문서 갱신", "sync", "디자인 토큰 업데이트", "피그마 바뀐 거 반영" 류 요청에 사용. Figma REST 덤프 → 자산 파악 → 이전 상태 비교 → 문서 재작성 → 검증 → 커밋·푸시까지 수행.
---

# sync — Figma 디자인 시스템 문서 동기화

Figma 원본이 바뀌었을 때 `design-system/`을 최신 상태로 재작성하는 엔드투엔드 워크플로우.

## 원칙 (필수)

- **JSON에서 확인 안 되는 값은 추측 금지 → `[확인 필요]`로 표시.**
- **4단계(문서 재작성) 시작 전에 3단계(비교 결과)를 사용자에게 보여주고 진행 여부를 확인받는다.**
- **각 단계 완료 시 진행 상황을 보고**한다.
- API 재호출은 **1단계에서만**. 이후 모든 파싱은 로컬 `sources/figma-raw.json`만 사용.
- 값 표기: 색은 `#RRGGBB`(+반투명 `@0.NN`), 크기 px. 변수 기반이라 토큰명을 못 얻으면 팔레트 매칭으로 표기하고 그 사실을 명시.

## 참고 상수 (변동 가능 — 매번 재확인)

- **fileKey:** `UsCx1wPybDpRRBglYY5Nmx` (0단계에서 CLAUDE.md·index.md 기록과 대조)
- **페이지:** `1. Logo`, `2. Foundation`(색·타이포 스와치), `3. Component`(UI 컴포넌트)
- **Foundation Color 프레임:** 스와치=라벨(TEXT)+색(rect fill) 쌍으로 `이름↔값` 추출
- **Foundation Typography 표:** 각 행에 스타일 적용 + `Size/Weight/LH/LS/용도` 라벨
- **컴포넌트 19단위**(직전 sync 기준 node ID, 이름 변경·ID 변동 가능하므로 2단계에서 재조사):
  로고 Attention·Signature / Button·Input·Input Case·Checkbox·Radio·Dropdown List·Search Filter·Tab·Tag·Table Cell·Toast Popup·Carousel·Sidebar·Breadcrumb·Dashboard Card·Header·Pagination

---

## 0. 필수 정보 확인

- `.env`에 `FIGMA_TOKEN` 존재 확인. 없으면 사용자에게 요청하고 중단.
- 대상 fileKey가 `CLAUDE.md`/`design-system/index.md`에 기록된 키와 같은지 확인.
  - 다르면 **사용자에게 어느 파일을 대상으로 할지 물어보고** 시작.

## 1. 덤프 (API 재호출은 여기서만)

```bash
cd <repo-root>
set -a; . ./.env; set +a
rm -f sources/figma-raw.json; mkdir -p sources
curl -s -w '%{http_code}\n' -H "X-Figma-Token: $FIGMA_TOKEN" \
  "https://api.figma.com/v1/files/$FILEKEY" -o sources/figma-raw.json
```
HTTP 200과 `lastModified` 확인 후 보고. (`sources/`는 gitignore — 커밋 안 됨)

## 2. 자산 전수 파악 (표로 보고)

로컬 JSON만 파싱해서 보고:
- 스타일 수: TEXT / FILL / EFFECT를 **local(`remote=False`) vs remote(`remote=True`) 분리** 집계.
  - **정본 판정은 local 스타일만**으로 한다. remote 스타일(같은 이름 중복·legacy·px-named 포함)은 다른 파일/라이브러리에서 **붙여넣은 콘텐츠(예: 예시 화면)가 참조**하는 것일 수 있으니 신규/중복 생성으로 오판하지 말 것.
- COMPONENT / COMPONENT_SET 수 (트리 기준)
- 페이지별 노드 수 / 컴포넌트 수
- 컴포넌트셋+독립 컴포넌트 목록(이름 + node ID + **소속 페이지**). **정본 페이지(`1. Logo`·`3. Component`) 밖의 컴포넌트는 `[정본 외]`로 표시** — 예시/화면 작업 페이지에 붙여넣다 딸려온 중복 메인 컴포넌트일 수 있음(인스턴스와 구분: `componentId`가 있으면 INSTANCE, `None`이면 메인 COMPONENT).

```python
import json;from collections import Counter
d=json.load(open("sources/figma-raw.json"));doc=d["document"];sm=d["styles"]
CANON_PAGES={"1. Logo","3. Component"}
# 스타일: local vs remote 분리
loc=Counter(v["styleType"] for v in sm.values() if not v.get("remote"))
rem=Counter(v["styleType"] for v in sm.values() if v.get("remote"))
print("local(정본 후보):",dict(loc)," | remote(참조):",dict(rem))
pages=[c for c in doc["children"] if c["type"]=="CANVAS"]
sets=[];stand=[]
def w(n,pt,page):
    if n["type"]=="COMPONENT_SET":sets.append((n["id"],n["name"],page,len([c for c in n.get("children",[]) if c["type"]=="COMPONENT"])))
    if n["type"]=="COMPONENT" and pt!="COMPONENT_SET":stand.append((n["id"],n["name"],page,"[정본 외]" if page not in CANON_PAGES else ""))
    for c in n.get("children",[]):w(c,n["type"],page)
for p in pages:w(p,"CANVAS",p["name"])
# 정본 외 컴포넌트는 중복 여부 경고
```

## 3. 이전 상태와 비교 → **사용자 확인 지점**

- 직전 커밋의 문서(tokens/*, components/*)와 새 덤프를 대조:
  - 추가/삭제/변경된 **스타일**(이름·값), 추가/삭제/이름변경된 **컴포넌트**, 값이 바뀐 토큰
- **변경이 없으면 "변경 없음"으로 종료** (4단계 이하 생략).
- 변경이 있으면 요약을 **사용자에게 보여주고 진행 여부를 확인**한 뒤 4단계로.

## 4. 문서 갱신 (확인 후)

`design-system/` 재작성. 각 문서 500줄 이내, 초과 시 분할.

**tokens/color.md** — Foundation Color 프레임에서 팔레트(이름+값) 추출. Primary/System/Grey 그룹. Foundation 밖 시맨틱/레거시 FILL 스타일은 제외하되 존재는 하단에 기록.

**tokens/typography.md** — Foundation Typography 표 기준. 실제 Figma 스타일명을 주 토큰명, 별칭·용도 병기. Pretendard/LH/LS 공통값 명시. 스펙 라벨과 실측 px이 다르면 하단 "스펙-실측 불일치"에 기록. Foundation 밖(ko/en/legacy/px-named)은 제외.

**tokens/spacing.md** — `3. Component` 페이지 변수 바인딩에서 radius/padding/gap 값 스케일 집계(변수 토큰명은 REST 미제공 → `[확인 필요]`).

**tokens/effect.md** — EFFECT 스타일 → x/y/blur/spread/color/용도.

**components/[이름].md** — 각 단위마다: 노드 ID·페이지 / variant 속성·전체 목록 / variant별 크기·padding·radius·gap / 적용 텍스트·컬러(팔레트 매칭)·이펙트 토큰 / 하위 구조. 아래 생성기 사용:

```python
# sources/gen_component.py 를 만들어 재사용. 핵심 로직:
# - PAL: 팔레트 HEX→이름 매핑(Blue-700 #003EFF … Grey-50 #FFFFFF)으로 fill/stroke 표기
# - collect(): variant 서브트리에서 styles.text/fill/effect 스타일명 + fills/strokes hex 수집
# - geom(): absoluteBoundingBox W×H, padding(TRBL), cornerRadius/rectangleCornerRadii, itemSpacing
# - COMPONENT_SET이면 자식 COMPONENT들을 variant로, 아니면 단일
# 직전 sync의 sources/gen_component.py 가 있으면 재사용, 없으면 재작성.
```

## 5. 검증

- **legacy 토큰 잔존 검사** (컴포넌트 문서 + 19단위 정의 내부):
  ```bash
  grep -rqE '(Body/Body[0-9]-[0-9]+-|Caption/Caption[0-9]-[0-9]+-|text-xs-normal|ko/[가-힣]|en/[a-z])' design-system/components/ && echo "잔존" || echo "clean"
  ```
  (⚠️ `grep|sort|uniq`의 종료코드는 uniq 것이라 오탐 → `grep -rq`로 판정)
  잔존 시 컴포넌트/variant/레이어/토큰을 특정해 보고.
- **index.md 링크 유효성**: 링크된 `tokens/*`·`components/*`(공백은 `%20` 디코드) 파일 존재 확인.

## 6. 진행 로그

`design-system/extraction-plan.md` 하단 진행 로그에 한 줄 추가: `- YYYY-MM-DD(sync): 변경 요약 / clean 여부`.

## 7. 커밋·푸시

- 한국어 커밋 메시지 + 변경 요약. 끝에:
  `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`
- `git add design-system/ && git commit && git push origin main`
- (이 레포는 git config/add 무확인 실행 허용. push는 사용자가 요청/승인한 흐름에서만.)

---

## 완료 보고 형식

타이포/컬러/이펙트/스페이싱 변경 요약 · 갱신한 컴포넌트 수 · legacy 검증 결과(clean 여부) · 남은 `[확인 필요]` · 커밋 해시.
