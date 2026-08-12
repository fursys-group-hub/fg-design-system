---
name: design-qa
description: 피그마 파일이 시디즈 디자인 시스템 정본(design-system/)을 지키는지 검사하고, 위반 항목을 컴포넌트→variant→레이어 단위로 보고한다. "디자인 QA", "피그마 정본 검사", "design-qa", "디자인 시스템 위반 검사", "타이포/컬러 규칙 지키는지 확인" 류 요청에 사용. REST 덤프 → 타이포·컬러·컴포넌트·스페이싱·네이밍 검사 → 심각도별 보고 → audits/ 저장. 피그마는 읽기만 하고 수정하지 않는다.
---

# design-qa — 피그마 vs 시디즈 디자인 시스템 정본 검사

작업 중인 피그마 파일이 `design-system/` 정본을 지키는지 검사하고, 위반을 컴포넌트→variant→레이어 단위로 잡아 심각도별로 보고하는 읽기 전용 워크플로우.

## 원칙 (필수)

- **피그마를 수정하지 않는다. 읽기와 보고만 한다.**
- JSON에서 판단 불가한 항목은 **추측 금지 → `[확인 필요]`로 표시.**
- 위반이 **0건이면 "clean"으로 명확히 보고**한다.
- 각 위반에 대해 **정본의 어느 규칙을 근거로 하는지 문서명**(예: `tokens/typography.md`)을 함께 표기한다.
- 정본 기준은 항상 `design-system/index.md`를 먼저 읽고 → `tokens/`, `components/`를 로드해서 사용. 정본을 외워서 판단하지 않는다.
- 값 표기: 색은 `#RRGGBB`(+반투명 `@0.NN`), 크기 px.

## 참고 상수 (변동 가능 — 매번 재확인)

- **DS 파일 키:** `UsCx1wPybDpRRBglYY5Nmx` (자체 점검 모드 판별 기준)
- **정본 타이포 14종:** Title1~5-SemiBold, Body1~4, Caption1~5 (Pretendard / LH 150% / LS 1%)
- **정본 팔레트:** Blue-700/500/100, Red-600/100, Grey-900~50 — 정확한 값은 `tokens/color.md`에서 로드
- **컴포넌트 로컬 색 allowlist (색+컴포넌트 쌍 — 색상만 X):** 근거 `tokens/color.md` "컴포넌트 로컬 색". 아래 쌍은 **지정 컴포넌트 서브트리 안**에서만 통과, 그 외 위치에서 발견되면 위반.
  - `#10C266`, `#E7F6E7` — **Tag** (Color=Green)
  - `#F5CA1D` — **Tag** (Color=Yellow) · **Toast Popup** (State=Alert)
  - `#FCF7DF` — **Tag** (Color=Yellow, State=Light)
- **로고 자산 색 (색+노드범위 — UI 색 아님):** 근거 `tokens/color.md` "로고 자산 색".
  - `#1D1D1B` — **Signature 로고 벡터 `66:3931`~`66:3935` 및 그 인스턴스**(노드 id에 해당 base id 포함)에서만 통과. 그 외 노드에서 fill로 발견되면 **위반**.
- **가이드/문서 색 (검사 전면 제외 — 건수만 집계):** 근거 `tokens/color.md` "가이드/문서 색". 위치 무관 검사 제외, 보고엔 제외 건수만.
  - `#8A38F5`(세트/인스턴스 테두리) · `#9747FF`(플레이스홀더) · `#F9F4FF`(정리용 배경)
- **최소 크기 규칙:** Caption4·5(8·10px)는 뱃지/태그/아이콘 라벨 전용, 본문 사용 금지

---

## 0. 필수 정보 확인

- 검사 대상 **파일 키**와 **페이지/프레임 범위**를 확인. 없으면 사용자에게 묻고 중단.
- `.env`에 `FIGMA_TOKEN` 존재 확인. 없으면 사용자에게 요청하고 중단.
- **모드 판별:**
  - **자체 점검** = 대상이 DS 파일(`UsCx1wPybDpRRBglYY5Nmx`)인 경우
  - **실무 점검** = 다른 작업 파일인 경우
- 정본 로드: `design-system/index.md` → `tokens/`(color·typography·spacing·effect) + `components/`. 검사 내내 이 로드본만 기준으로 삼는다.

## 1. 대상 덤프

- 대상이 **DS 파일이면** 기존 `sources/figma-raw.json`을 재사용 (재호출 안 함).
- 그 외에는 REST 호출로 `sources/qa-target.json`에 저장:

```bash
cd <repo-root>
set -a; . ./.env; set +a
mkdir -p sources
curl -s -w '%{http_code}\n' -H "X-Figma-Token: $FIGMA_TOKEN" \
  "https://api.figma.com/v1/files/$FILEKEY" -o sources/qa-target.json
```

HTTP 200과 `lastModified` 확인 후 보고. (`sources/`는 gitignore — 커밋 안 됨)
0단계에서 정한 페이지/프레임 범위로 검사 서브트리를 한정한다.

## 2. 검사 항목 — 각각 위반 건수와 위치(컴포넌트/variant/레이어)를 수집

로컬 JSON만 파싱. 각 위반은 `컴포넌트 / variant / 레이어 / 현재값 → 권장값 / 근거 문서`를 기록한다.

**T1. 타이포 준수** — 근거: `tokens/typography.md`
- 정본 14종(Title1~5-SemiBold, Body1~4, Caption1~5) 외 텍스트 스타일 사용
- 스타일 미적용(스타일 연결 없이 크기·굵기 직접 지정 — `styles.text` 없이 `style.fontSize/fontWeight`만 있는 TEXT 노드)
- 정본 외 폰트 크기 사용
- 최소 크기 위반(본문에 8·10px 사용 — Caption4·5는 뱃지/태그/아이콘 라벨만 허용)

**T2. 컬러 준수** — 근거: `tokens/color.md`
- 팔레트(Blue-700/500/100, Red-600/100, Grey-900~50) 외 hex 직접 입력
- 팔레트와 근사하지만 다른 값 사용(예: `#FEFEFE` vs Grey-50 `#FFFFFF`) → 근사 매칭으로 후보 팔레트명 병기
- **허용 판정 순서(색이 팔레트 밖일 때):** ① **가이드/문서 색**이면 → 검사 제외(건수만 집계). ② **로고 자산 색**이 지정 노드범위 안이면 → 통과. ③ **컴포넌트 로컬 색 allowlist** (색+컴포넌트) 쌍이 해당 컴포넌트 서브트리 안이면 → 통과. ④ 위 어디에도 안 들면 아래 오검출 방지 필터 적용 후 위반 후보.
  - allowlist·로고색은 **색상만으로 통과시키지 않는다**(반드시 색+컴포넌트/노드범위). 같은 색이라도 지정 범위 밖이면 위반.
- **오검출 방지(필수):** ① **노드 `visible=false`(및 상위 숨김) 서브트리는 검사 제외.** ② **변수/스타일 연결(boundVariables·styles.fill/stroke)된 색은 토큰으로 간주** → 원시 hex 위반 아님(detached 색만 후보). ③ **컴포넌트 정의(COMPONENT/COMPONENT_SET) 밖의 문서·스펙·가이드·견본 프레임 색은 컴포넌트 위반으로 보고하지 않음**(별도 "문서 영역"으로만 표기). ④ fill·stroke만 색으로 카운트(effect 색 제외), 반투명은 `paint.opacity`/`color.a`를 병기.

**T3. 컴포넌트 준수** — 근거: `components/*.md`
- 라이브러리 인스턴스가 아니라 직접 그린 유사 요소(INSTANCE 아닌데 정본 컴포넌트와 형태·이름이 유사)
- 인스턴스인데 오버라이드로 정본과 다르게 변형된 것(`overrides`/detached 속성 확인, 판단 불가 시 `[확인 필요]`)

**T4. 스페이싱 준수** — 근거: `tokens/spacing.md`
- spacing.md 스케일 외 padding/gap/radius 값(변수 바인딩 토큰명은 REST 미제공 → 값 기준 대조, 불명확 시 `[확인 필요]`)

**T5. 네이밍 컨벤션** — 근거: 프로젝트 네이밍 규칙(정보 등급)
- variant 속성명 오타(예: `Varient` → `Variant`)
- 레이어명이 `Frame 1000006124` 같은 기본값으로 방치된 것

## 3. 보고

- **심각도별 분류:**
  - **위반** — 정본과 명백히 어긋남 (T1~T4 명백 케이스)
  - **주의** — 정본에 없지만 의도적일 수 있음 (근사 컬러, 오버라이드 등)
  - **정보** — 네이밍 등 (T5)
- **각 항목을 표로:** `컴포넌트 / variant / 레이어 / 현재값 → 권장값 / 근거 문서`
- **요약:** 검사한 노드 수, 항목(T1~T5)별 위반 건수, `[확인 필요]` 건수, **clean 여부**

## 4. 결과 저장

- `design-system/audits/qa-{대상명}-{YYYY-MM-DD}.md`로 저장 (디렉터리 없으면 생성).
- 파일 상단에 대상 파일 키·모드(자체/실무)·검사 범위·덤프 `lastModified` 기록.
- **커밋은 사용자 승인 시에만.** 승인 시 한국어 커밋 메시지 + 끝에:
  `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`

---

## 완료 보고 형식

모드(자체/실무) · 검사한 노드 수 · T1~T5 항목별 위반 건수(위반/주의/정보) · clean 여부 · 남은 `[확인 필요]` · 저장 경로.
