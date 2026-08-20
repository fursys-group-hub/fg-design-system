# CLAUDE.md

> # ⚠️ 필수 — 생성물 저장 위치
> **모든 생성물(화면·컴포넌트·HTML·목업 등)은 `~/Desktop/sidiz-output/`에 저장한다.** 폴더가 없으면 만든다.
> **저장소 내부(루트·`design-system/`·`dist/`)에는 어떤 생성물도 만들지 않는다.**
> 이 규칙은 **추론·예외 없이 항상** 적용한다. 다른 위치가 자연스러워 보여도 위 경로를 쓴다.

이 저장소는 **SIDIZ(시디즈) 디자인 시스템**의 정본(`design-system/`)과 실무자 배포물(`dist/sidiz/`)을 관리하는 곳이다.

> 이 파일의 UI 지침·규칙 요약은 `/export` 시 `dist/sidiz/` 기준으로 동기화된다. 마지막 동기화: 2026-08-20.

> ## ⚠️ 절대 원칙 — 정본 15색 · 14종 (예외 없음)
> 정본은 **컬러 15색(Blue 3 / Red 2 / Grey 10) + 타이포 14종(Title1~5, Body1~4, Caption1~5)**뿐이다. 이 밖의 색·크기·굵기는 존재하지 않는다(근사·신규·중간·예외 토큰 금지, 팔레트 확장 금지). 정본 밖 값이 발견되면 오류이자 정본 토큰 교정 대상이며, `design-qa`는 이를 "위반"으로 분류한다.
> **화면 제작 시 `dist/sidiz/tokens.css`의 클래스(타이포 14종 + 컴포넌트 클래스)만 사용하고 `font-size`·`padding`·`height`를 직접 지정하지 않는다.** 필요한 클래스가 없으면 임의로 만들지 말고 관리자에게 알린다. 유일한 예외: 문서화된 컴포넌트 로컬 확장색(Tag Green/Yellow·Toast Alert)뿐.

## UI/화면을 생성·수정할 때 (필수)

화면·컴포넌트·스타일 등 UI가 포함된 결과물을 만들거나 고칠 때는 **반드시 아래 두 문서를 먼저 읽고 그대로 따른다.**

- **`dist/sidiz/Design.md`** — 값·규격(색·타이포·스페이싱·이펙트·컴포넌트 명세)의 통합 규격서.
- **`dist/sidiz/design-principles.md`** — 화면 조립·판단 기준(레이아웃·위계·패턴).

스타일은 `dist/sidiz/tokens.css`의 CSS 변수·클래스로만 적용한다. HTML 생성 시 `Design.md`의 **Pretendard 웹폰트 로드 1줄**을 반드시 포함한다.

- **생성물은 반드시 `~/Desktop/sidiz-output/`에 저장한다** (문서 최상단 규칙). 저장소 안에 만들지 않는다.

> **옛 전역 플러그인/스킬은 폐기됐다.** `~/.claude/skills/sidiz-design-system` 및 그 규격(Centra 폰트, 좌측 아이콘 레일, gray-100 캔버스, admin-dashboard 스캐폴드 등)은 **더 이상 사용하지 않는다.** 옛 규격으로 화면을 만들지 않는다.

## 반드시 지킬 원칙 (요약 — 상세는 Design.md · design-principles.md)

- **폰트:** Pretendard 단일. LH 150%, LS 1%. Centra/Inter/Roboto/system 기본 폰트 금지.
- **색:** 브랜드 포인트 `Blue-700(#003EFF)`은 강조/선택/링크에만 절제 사용. 에러 `Red-600`. 나머지는 Grey 10단계. 팔레트 밖 색(보라/그라데이션 등) 금지. **Blue를 버튼 채움 배경으로 쓰지 않는다.**
- **버튼:** 결정 버튼은 화면당 1개, Primary=`Grey-900`. 파란 채움 버튼을 기본으로 쓰지 않는다.
- **구분:** border 우선(hairline `Grey-200`). 그림자는 떠 있는 표면(드롭다운/토스트/팝오버/카드 부양)에만.
- **배경:** 앱·페이지 배경은 **흰색(`Grey-50`)**. **회색 채움 캔버스(`Grey-100` 등) 금지** — `Grey-100`은 테이블 헤더 등 지정 표면에만.
- **radius:** 버튼/인풋 4~6px, 태그·칩·원형은 pill. 임의값 금지.
- **최소 크기:** `Caption4·5`(8·10px)는 뱃지/태그/아이콘 라벨 전용, 본문 금지.
- **컴포넌트 로컬 색**(Tag Green/Yellow, Toast Alert 노랑)은 `Design.md`에 문서화된 해당 컴포넌트 안에서만.
- **화면 조립**(화면 골격·필터·요약 카드·테이블·모달·피드백·색 사용)은 `design-principles.md`를 따른다.
- **로고**는 `Design.md`의 인라인 SVG(Attention)/Signature를 사용하고, "SIDIZ" 워드마크 텍스트로 대체하지 않는다.

## 저장소 구조

- `design-system/` — **정본(source of truth).** Figma에서 추출한 토큰(`tokens/`)·컴포넌트(`components/`)·화면 조립 원칙(`design-principles.md`)·라우터(`index.md`). 값의 최종 원본은 Figma `시디즈_디자인 시스템`.
- `dist/sidiz/` — **실무자 배포물**(정본에서 `/export`로 생성). `Design.md`·`design-principles.md`·`tokens.css`·`CLAUDE.md`·`README.md`. **자동 생성물이므로 직접 수정 금지** — 값 변경은 정본에서 하고 다시 export 한다.
- 정본과 배포물이 다르면 **정본이 우선.**

## 스킬

- `/sync` — Figma 재덤프 → `design-system/` 정본 갱신(local/remote 분리 검사 포함).
- `/design-qa` — 피그마·결과물이 정본 규격을 지키는지 검사(팔레트·타이포·컴포넌트·스페이싱).
- `/export` — 정본 → `dist/sidiz/` 배포물 생성 + **루트 CLAUDE.md 동기화**.

## design-system/ 문서 편집 원칙 (관리자용)

- **추측 금지.** 확실치 않은 값은 `[확인 필요]`로 표시하고 지어내지 않는다.
- 토큰 항목 형식: **이름 / 값 / 용도 / 사용 규칙**.
- 각 문서 500줄 이내(넘으면 분할).
- `design-principles.md`는 `/sync` 대상이 아니며 관리자가 직접 수정한다.
- 디자인이 바뀌면 정본을 고친 뒤 `/export`로 배포물과 이 CLAUDE.md를 재생성한다.
