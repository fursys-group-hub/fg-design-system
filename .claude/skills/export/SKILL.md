---
name: export
description: design-system/ 정본 문서를 실무자용 배포물(dist/sidiz/)로 가공한다. 정본 → 배포물 단방향이며 역방향은 없다. tokens 4종 + components 19개를 통합 마크다운·tokens.css·CLAUDE.md·README.md로 변환한다. "디자인 시스템 배포", "export", "dist 생성", "배포물 만들어줘", "tokens.css 뽑아줘", "실무자용으로 내보내줘" 류 요청에 사용. 정본은 읽기만 하고 수정하지 않는다.
---

# export — 정본(design-system/) → 실무자 배포물(dist/sidiz/)

`design-system/` 정본 문서를 Cowork/클로드 챗/클로드 코드 실무자가 바로 쓰는 배포물로 가공하는 워크플로우.

## 원칙 (필수)

- **방향은 항상 정본 → 배포물.** `design-system/`을 읽어 `dist/sidiz/`를 생성한다. **역방향(배포물 → 정본)은 없다.**
- **정본을 수정하지 않는다.** `design-system/` 아래 파일은 읽기 전용. 쓰기는 `dist/` 아래로만.
- **값을 지어내지 않는다.** 정본에 없는 값은 만들지 않는다. 정본의 `[확인 필요]` 항목은 **CSS에 넣지 않고 별도 보고**한다.
- **자동 생성물 명시.** 모든 생성 파일 상단에 `자동 생성 파일 — 원본은 design-system/. 직접 수정 금지.`를 남긴다.
- **버전 스탬프(필수).** 4종 산출물 **최상단**에 `버전: {YYYY-MM-DD} / 생성 커밋: {짧은 해시}`를 박는다.
  - 날짜 = export **실행일**, 해시 = `git rev-parse --short HEAD` (실행 시점 HEAD).
  - `.md` 3종은 최상단 **헤더 줄**(blockquote), `tokens.css`는 최상단 **주석**.
  - 정확한 provenance를 위해, 스탬프할 소스 변경분은 **export 전에 커밋**해 HEAD를 확정한 뒤 실행한다(dist 재생성 커밋은 그 다음). 즉 스탬프 해시 = 배포물이 생성된 **정본/스킬 소스 커밋**.
  - 목적: 수십~수백 명 배포 환경에서 실무자가 자신이 보는 문서의 최신 여부를 확인.
- 값 표기: 색은 `#RRGGBB`(+반투명 `@0.NN`), 크기 px.
- 정본 로드는 항상 `design-system/index.md`를 먼저 읽고 → `tokens/` + `components/`를 로드한다. 외워서 변환하지 않는다.

## 참고 상수 (변동 가능 — 매번 정본에서 재확인)

- **정본 토큰 4종:** `tokens/color.md`, `tokens/typography.md`, `tokens/spacing.md`, `tokens/effect.md`
- **정본 컴포넌트 19종:** `components/*.md` (index.md 컴포넌트 표 기준)
- **타이포 14종:** Title1~5-SemiBold, Body1~4, Caption1~5 (Pretendard / LH 150% / LS 1%)
- **최소 크기 규칙:** Caption4·5(8·10px)는 뱃지/태그/아이콘 라벨 전용, 본문 사용 금지

---

## 0. 사전 확인

- **정본 최신성:** `design-system/extraction-plan.md`의 **마지막 로그**를 확인해 정본이 최신인지 본다. 오래됐거나 진행 중이면 사용자에게 알리고 진행 여부를 묻는다.
- **미해결 위반 확인:** `design-system/audits/`의 **가장 최근 design-qa 결과**를 읽는다. **미해결 "위반"(명백)이 있으면 경고**하고, 그대로 배포할지 사용자에게 묻는다. (주의·정보 등급은 진행 가능, 단 보고에 언급)
- 정본 로드: `index.md` → `tokens/`(color·typography·spacing·effect) + `components/` 19종. 로드본만 변환 소스로 삼는다.
- `dist/sidiz/` 디렉터리 준비(없으면 생성).

## 1. `dist/sidiz/Design.md` 생성

- tokens 4종 + components 19개를 **한 파일로 통합**.
- **구조:** 개요 → **웹폰트 로드** → 컬러 → 타이포 → 스페이싱 → 이펙트 → 컴포넌트별 명세 → **로고 SVG**.
- 각 값에 **사용 규칙(언제 쓰고 언제 안 쓰는지)을 함께** 기재해 AI가 읽고 화면을 만들 수 있게 한다.
- **Pretendard 웹폰트 로드 안내(필수):** 생성하는 HTML `<head>`에 아래 한 줄과 body 폰트 지정을 포함하라는 지침을 개요/폰트 섹션에 명시한다.
  - `<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css">`
  - `body { font-family: 'Pretendard', sans-serif; }`
- **로고 SVG 섹션(필수):** `design-system/assets/attention-black.svg`·`attention-white.svg`의 **인라인 SVG 코드**를 그대로 싣는다(배포본만 읽어도 로고를 쓸 수 있게). Black=밝은 배경, White=어두운 배경.
- 상단에 **버전 스탬프**(원칙 참조) + `자동 생성 파일 — 원본은 design-system/` 명시 + 정본 덤프 기준(`lastModified`)을 남긴다.
- **상단 참조 1줄:** 버전 스탬프 아래에 `화면 조립·판단 기준은 design-principles.md 참조`를 넣는다(화면 조립 규칙은 별도 파일).
- 500줄을 넘으면 섹션 요약 위주로 압축하되, 토큰 값·컴포넌트 variant 목록·로고 SVG는 누락 없이 유지한다.

## 2. `dist/sidiz/tokens.css` 생성

정본 값을 CSS 커스텀 프로퍼티로 변환. `:root`에 정의한다.

- **컬러:** `--sidiz-color-*` (예: `--sidiz-color-blue-700: #003EFF;`). 정본 팔레트만.
- **타이포:** `--sidiz-font-*`(family/size/weight/line-height/letter-spacing) + **조합 클래스** `.title1 ~ .caption5`(14종).
- **스페이싱:** `--sidiz-space-*`(padding/gap 스케일), `--sidiz-radius-*`(radius 스케일).
- **이펙트:** `--sidiz-shadow-*`(Drop Shadow 2겹 합성, shadow/sm).
- **`[확인 필요]` 항목은 CSS에 넣지 않는다.** 대신 5단계 보고에 "CSS 제외 — 확인 필요" 목록으로 모아 보고한다.
- 상단 주석에 **버전 스탬프**(원칙 참조) + `자동 생성 파일 — 원본은 design-system/` 명시.

## 3. `dist/sidiz/CLAUDE.md` 생성

Cowork 사용자용 지침 파일. 최상단에 **버전 스탬프**(원칙 참조) + 자동 생성 명시.

- 핵심 지시: **"이 폴더의 `Design.md`(값·규격)와 `design-principles.md`(화면 조립·판단 기준)를 항상 참조하고, 그 규격·원칙대로 화면을 만든다."**
- 지켜야 할 원칙 명시:
  - **화면 조립은 `design-principles.md`** 를 따른다(레이아웃·위계·패턴). **값·규격은 `Design.md`.**
  - **정본 토큰만 사용** — `tokens.css` 변수/클래스로만 스타일. 임의 hex·폰트·radius 발명 금지. **단, `Design.md`에 문서화된 "컴포넌트 로컬 색"은 해당 컴포넌트에 한해 허용**(전역 토큰 아님, 다른 곳 사용 금지).
  - **최소 크기 규칙** — Caption4·5(8·10px)는 뱃지/태그/아이콘 라벨 전용, 본문 금지.
  - 브랜드 포인트 `Blue-700 #003EFF` 절제 사용, 기본 구분은 border(그림자는 떠 있는 표면만).
  - 컴포넌트는 `Design.md`의 명세·variant 범위 안에서만 사용.

## 4. `dist/sidiz/README.md` 생성

**실무자 온보딩 안내문.** 대상 독자 = 디자인 시스템을 처음 접하는 실무자(비개발자 포함).

- **문체:** 전체를 **존댓말 서술형**으로 쓴다(예: "저장소를 클론해 주세요", "접속하시면 바로 사용할 수 있습니다"). 개조식 명령문("클론한다", "실행할 것") 금지. **단, 명령어(git clone 등)와 코드 블록은 그대로** 둔다.
- **최상단:** 버전 스탬프(원칙 참조) + 자동 생성 명시.
- **구성(순서 고정):**
  1. **시작** — 이 문서가 무엇인지 + **버전 확인 방법**(최상단 스탬프의 날짜·커밋을 저장소 최신과 대조) 2~3줄. `Design.md`(값·규격)와 `design-principles.md`(화면 조립·판단 기준) 두 축을 함께 안내.
  2. **경로 A. 클로드 챗** — 회사 공유 프로젝트 링크 `https://claude.ai/project/019ff881-be01-75f1-921a-72c7db7b4f8e`로 접속해 바로 사용. 프로젝트에 디자인 시스템이 **이미 세팅**되어 있음(`Design.md`+`design-principles.md`)을 안내.
  3. **경로 B. 클로드 코드/터미널** — 저장소 클론(`git clone`), `git pull`로 최신화, `/sidiz-design-system`·`/design-qa` 스킬 사용법 간단 안내. 화면 조립 시 `design-principles.md`를 함께 참조하도록 안내.
  4. **경로 C. Cowork** — 이 `dist/sidiz/` 폴더를 작업 폴더로 지정(CLAUDE.md 자동 적용). 폴더에 `Design.md`·`design-principles.md`가 함께 있음을 안내. *(환경 3종 중 세 번째)*
  5. **공통 규칙** — 정본 토큰만 사용 · 문서 **직접 수정 금지**(수정 요청은 디자인 시스템 관리자에게) · 컴포넌트 로컬 색은 문서화된 범위에서만 · **값은 `Design.md`, 화면 조립은 `design-principles.md`** 기준.
  6. **문의** — 관리자 연락처 `@커머스DX팀 이수지`.
- **실제 값(반영됨):** 프로젝트 링크 = `https://claude.ai/project/019ff881-be01-75f1-921a-72c7db7b4f8e` · 관리자 연락처 = `@커머스DX팀 이수지`. 값이 바뀌면 이 규칙을 갱신한다.

## 5. `dist/sidiz/design-principles.md` (독립 복사)

정본 `design-system/design-principles.md`를 **그대로 복사**한다(값 변환·요약 없음). **`Design.md`에 병합하지 않는다** — 화면 조립 규칙은 별도 파일로 유지한다.

- 복사본 **최상단에 버전 스탬프**(원칙 참조, 다른 산출물과 동일 날짜·해시) + `자동 생성 파일 — 원본은 design-system/design-principles.md` 명시.
- 본문은 정본과 동일하게 유지(토큰·컴포넌트 이름 참조, 값 미기재).

## 6. 루트 `CLAUDE.md` 동기화

저장소 루트 `CLAUDE.md`가 **새 배포물을 가리키도록** 유지한다(모든 터미널 세션이 이 파일을 로드하므로, 옛 규격이 남으면 세션이 오염된다).

- **UI 작업 지침**이 `dist/sidiz/Design.md`(값·규격) + `dist/sidiz/design-principles.md`(조립 기준)를 먼저 읽고 따르도록 명시되어 있는지 확인·갱신.
- **핵심 규칙 요약**(폰트=Pretendard, 팔레트, Grey-900 결정 버튼, border 우선, 로컬 색, 화면 조립=design-principles)이 현재 dist와 일치하는지 확인.
- **옛 플러그인/전역 스킬 참조 없음 확인:** `~/.claude/skills/sidiz-design-system`, Centra, 아이콘 레일, gray-100 캔버스, admin-dashboard, plugin.json, "두 위치 동기화" 등 구세대 문구가 남아 있으면 제거.
- 상단 "마지막 동기화" 날짜를 export 실행일로 갱신.
- 저장소 구조·스킬 안내 등 리포 고유 섹션은 유지(전체 재생성이 아니라 지침·규칙 정합만 맞춘다).

## 7. 검증 및 보고

- **생성 결과:** 각 파일 경로·크기(줄 수/바이트), 통합 문서에 포함된 **토큰 수·컴포넌트 수**.
- **개수 일치 검증:** 정본 토큰 4종 / 컴포넌트 19종과 배포물 포함 개수가 **일치하는지** 대조. 불일치 시 누락 항목 명시.
- **CSS 제외 목록:** `[확인 필요]`라 tokens.css에 넣지 않은 항목을 모아 보고.
- **미해결 위반:** 0단계에서 확인한 design-qa 미해결 위반이 있으면 재고지.
- **커밋·푸시는 사용자 승인 시에만.** 승인 시 한국어 커밋 메시지 + 끝에:
  `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`

---

## 완료 보고 형식

정본 최신성·미해결 위반 여부 · 생성 파일 5종(Design.md·tokens.css·CLAUDE.md·README.md + design-principles.md 복사, 경로/크기) · 포함 토큰 수·컴포넌트 수 · 정본 대비 개수 일치 여부 · CSS 제외(확인 필요) 목록 · **루트 CLAUDE.md 동기화 여부** · 커밋 여부.
