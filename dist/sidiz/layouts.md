<!-- 자동 생성 파일 — 원본은 design-system/layouts.md. 직접 수정 금지. -->
> **버전: 2026-08-21 / 생성 커밋: `d992537`**
> 자동 생성 파일 — 원본은 `design-system/layouts.md`. 직접 수정 금지.

# Layouts — SIDIZ 화면 조립 레퍼런스

화면 유형별 골격·컴포넌트 조합·공통 치수를 정의한다. 개별 컴포넌트 값은 `components/*.md`, 값이 아닌 화면 판단 원칙은 `design-principles.md`가 정본이다.

> **출처·주의:** 구조·배치·컴포넌트 조합 맥락은 Figma `화면 예시` 페이지(실제 화면 35개)에서 추출했다. **색·로고·브랜드 고유 요소는 이 문서에 넣지 않으며, 반드시 시디즈 정본(`tokens/color.md`·로고 컴포넌트) 기준**으로 적용한다. (구조만 참고, 브랜드 값은 정본)

## 공통 레이아웃 치수

| 항목 | 값 | 비고 |
|---|---|---|
| 기준 캔버스 폭 | **1600** | 데스크톱 기준 |
| Sidebar 폭 | **256** | 좌우 padding 12 |
| 콘텐츠 영역 폭 | **1344** | = 1600 − 256 |
| Header 높이 | **50** | 좌우 padding 24, 하단 `Grey-200` 보더 |
| Contents padding | **top 24 / 좌우 32 / bottom 100** | |
| 콘텐츠 내부 폭 | **1280** | = 1344 − 64 |
| 본문(Contents) 배경 | **`Grey-100`** | v6: 본문은 회색 면 |
| 콘텐츠 카드 표면 | **`Grey-50`(흰색) + `Grey-200` 보더** | 카드/표만 흰 면 |

## 화면 레이아웃 (프레임·골격 클래스) — v6 정본

| 항목 | 값 |
|---|---|
| 전체 화면 폭 | 1600 |
| Sidebar 폭 | 256 (좌우 padding 12) |
| 본문 영역 폭 | 1344 (= 1600 − 256) |
| Contents padding | 상24 좌우32 하100 |
| 콘텐츠 폭 | **1280** (= 1344 − 64). 본문 컴포넌트는 1280 안으로 |
| 본문 배경 | **`Grey-100`** |
| 콘텐츠 카드 표면 | `Grey-50`(흰색) + `Grey-200` 보더 |

- 화면이 1600보다 넓어지면 콘텐츠는 1280 유지, **좌우 여백만 균등 증가**(`.sidiz-container`가 `max-width:1280px; margin:0 auto`).
- **골격 클래스:** `sidiz-app` → `sidiz-sidebar` + `sidiz-main`(`sidiz-header` + `sidiz-contents` → `sidiz-container`). 값 정본=`CLAUDE.md`「화면 레이아웃 규칙」·CSS=`sidiz-components.css`.

## 화면 골격 (레이어)

모든 표준 화면은 3(+2) 레이어로 구성:

1. **Sidebar**(고정, 256) — 로고 + 검색 + 메뉴. 검색창 H38.
2. **Header**(상단 바, 높이 50) — 좌측 `PanelLeft` 토글 · 우측 알림(`Bell`)·프로필
3. **Contents**(본문, 배경 `Grey-100`, padding 24/32/100) → `sidiz-container`(1280 중앙) → 페이지 타이틀 블록 → 본문
4. **Floating**(떠 있는 레이어) — 드롭다운·토스트 등
5. **Dimmed + Modal**(모달 시) — 전체 오버레이 + 중앙 모달

---

## 유형 1. 목록형 (테이블 중심)

가장 흔한 관리자 화면. 조회 → 목록.

**콘텐츠 순서** (`design-principles.md` §1과 동일 · 값 정본은 `CLAUDE.md`/`component-spec.md`):
1. 페이지 타이틀(`Title4`) + 우측 서브 문구(`Body4`/`Grey-400`)
2. 브레드크럼(우측 정렬)
3. **필터 카드** — Input Case 필드 1행 + 우측 조회 버튼(**Secondary Round**) · 상세 조회(**Text**)
4. (요약 카드) — 유형 3 참조
5. **테이블 섹션** — 섹션 타이틀(`Title5`)+건수(`Title5`/`Primary-600`, 단위 없음), 우측 액션 버튼 그룹 / Table(헤더 `Grey-100` 배경·`Caption1`, 셀 `Body2`, **No. 열 없음·첫 열 체크박스**) + 상태 `Tag` + 하단 `Pagination`(테이블 폭 기준 중앙)

## 유형 2. 상세형 (마스터-디테일)

목록에서 행 선택 → 상세. 상단 목록/요약 + 하단 상세 테이블(탭 전환 가능, `Tab` 컴포넌트).

## 유형 3. 대시보드형 (요약 카드)

- 상태별 **요약 카드 4~5개를 가로(HORIZONTAL) 1행**으로 배열한다. **세로(상하) 스택 금지.** 카드 간 **gap 8px**. 각 카드 = 상태 `Tag` + 큰 수치(`Title3`) + 단위(`Caption1`). **수치·단위 색은 카드 태그의 진한 색과 같게 맞춘다**(카드에 `sidiz-card--wait/--hold/--progress/--done/--fail` 부여 시 자동. 상세 규칙=`CLAUDE.md` 상태 태그 5범주).
- 카드 하단에 테이블/차트 섹션.

## 유형 4. 모달

- **Dimmed** 전체 오버레이 위 **Modal** 중앙 배치.
- 3단계: **소형**(확인·선택지, ~500 폭) / **중형**(폼·목록) / **대형**(일괄 등록).
- Modal = Title(padding 24) + 본문 + 완료 버튼(우측 하단 `Primary`/`Grey-900`).

## 유형 5. 인증·온보딩

- 좌우 분할: **Images(≈900)** + **Panel(≈700)**, 사이드바 없음.
- Panel에 로고(Signature/Attention) + 폼(Input Case). 로고는 시디즈 정본 로고 사용.

---

## 컴포넌트 중첩(조립) 규칙

정본 `3. Component` 하위 구조에서 확인된 실제 조합:

| 상위 | 하위 구성 |
|---|---|
| **Sidebar** | **브랜드 심볼(로고)** + 검색(Input, `grow 1`) + 메뉴(Tab / List, 항목 `fill`) |
| **Header** | 좌측 `Icon/PanelLeft`(+ 필요 시 로고) + 우측 `Icon/Bell`·프로필(`Icon/ChevronDown`) |
| **Toast Popup** | 콘텐츠(아이콘+텍스트) + **Button 인스턴스**, `SPACE_BETWEEN`(양끝) |
| **Input Case** | 라벨(`Body3`) + Input + 헬프/에러(`Body4`, 에러 `Red-600`) |
| **필터 카드** | Input Case 여러 개 1행(가로 auto-layout) + 조회 버튼(**Secondary Round**)·상세 조회(**Text**) |
| **테이블 행** | Table Cell 조합(Type: Checkbox/Text/Link/Button/Tag/Calendar…), **No. 열 없음·첫 열 체크박스**, 상태는 `Tag`, 링크는 밑줄 |
| **Dashboard Card** | `Tag`(상태) + 수치(`Title3`) + 단위(`Caption1`) |

> **브랜드 심볼(로고)은 `Design.md` §6의 정본 로고 SVG(Attention 심볼 / Signature)를 그대로 사용한다.** 아이콘 세트(Lucide 등)의 아이콘으로 로고를 대체하지 않으며, 로고 아트워크를 임의로 지어내지 않는다. (사이드바 상단·헤더·인증 화면 Panel의 브랜드 심볼 모두 동일)

> 화면 예시·목업은 **정본 컴포넌트의 인스턴스만으로** 조립한다(`design-principles.md` §8). 컴포넌트를 복제해 새 COMPONENT로 만들지 않는다.

## 화면 패턴 상세

> 관리자 콘솔(OMS류) 화면 구조. **마크업 정본은 `COMPONENTS.html`, CSS는 `sidiz-components.css`, 수치 근거는 `component-spec.md`, 값 규칙은 `CLAUDE.md`.** 아래는 배치 순서 요약이며, 값이 어긋나면 이 문서가 아니라 위 정본을 따른다.

### 페이지 타이틀 블록
- 좌측: 페이지 타이틀 `Title4`(16/600/Grey-900) + 우측 서브 문구 `Body4`(12/400/Grey-400), baseline 정렬, gap 8. 서술형은 마침표로 끝낸다.
- 우측 끝: Breadcrumb 우측 정렬(`Body2`/Grey-400, 현재 페이지 `Body1`/Grey-900).

### 필터 카드
- 필드 1행(폭은 가변 분배), 라벨은 인풋 상단 `Caption1`(11/600/Grey-500) + 필수표시 `*` Red-600.
- 우측 끝: "상세 조회" **Text 버튼**(`Body3`) + 조회 **Secondary Round 버튼**(흰 배경+Grey-200 보더). **Primary 검정 아님.**
- 카드 하단 중앙에 접기 토글: 24 원형, Grey-200 보더, ChevronUp/Down.
- 기간 필드만 고정(프리셋 드롭다운 136 + gap4 + 날짜 범위 인풋 216), `0000/00/00 - 0000/00/00` 한 줄 유지(2개로 쪼개지 않음).

### 요약 카드 행 (현황 카드)
- Dashboard Card 4~5개 가로 1행, gap 8. 카드 = 상태 태그 + 수치(`Title3`) + 단위(`Caption1`).
- **수치·단위 색은 카드 태그의 진한 색과 같게** 맞춘다(카드에 `sidiz-card--wait/--hold/--progress/--done/--fail` 부여 시 자동). 상세 규칙=`CLAUDE.md` 상태 태그 5범주.

### 섹션 타이틀 + 건수
- 섹션 타이틀 `Title5`(14/600/Grey-900) + 건수 `Title5`(14/600/Primary-600), gap 4, **단위를 붙이지 않는다**.
- 우측: 액션 버튼 그룹(Secondary 나열), 최우선 액션 1개만 Primary(Grey-900).

### 목록 테이블
- Header: Grey-100 배경, `Caption1`/Grey-400, 컬럼 구분 hairline Grey-200.
- Cell: `Body2`/Grey-900, 행 구분 Grey-200 hairline, 행 높이 38.
- 체크박스 컬럼 좌측 고정, 상태 컬럼은 태그, URL과 상세 링크는 밑줄(Grey-900).
- 합계 행: Grey-100 배경, `Body1`.
- 하단 Pagination 중앙 정렬.

### 마스터 디테일
- 상하 분할: 상단 목록 + 하단 상세 섹션(탭 전환은 Tab/Line variant, 선택 탭 Grey-900 + 하단 Primary-600 2px).
- 좌우 분할: 좌측 목록 + 우측 상세 폼 패널(Grey-200 보더 카드), 패널 우상단에 저장 Primary 버튼.
- 상세 폼: 섹션 타이틀 `Title5`(14/600) 단위로 구분, 필드는 2열 그리드(Input Case), 읽기 전용 필드는 Grey-200 배경 + Grey-400 텍스트(Input Disabled와 동일).

### 빈 상태 (조회 결과 없음)
- 목록 영역 중앙: 아이콘(Lucide, 24~32, Grey-400) + "조회 결과가 없습니다" `Body1`/Grey-900 + 보조문 `Body4`/Grey-400. 목록이 0건이면 목록 액션 버튼은 Disabled 상태로.

### 헤더 우측
- 알림 Bell 20×20 + 미확인 뱃지(Red-600) + 프로필 보더 박스(이름 `Body1`/Grey-900, 역할 뱃지 `Caption1`/Grey-400 + Grey-100 배경, ChevronDown 16).

### 플로팅 버튼
- 우하단 원형 버튼(맨 위로 등): Grey-50 배경 + Grey-200 보더 또는 Grey-900 배경 + 흰 아이콘, 9999 라운드.

## 확인 필요

- 화면 예시는 **타 브랜드 작업물**에서 구조만 추출했다. 위 치수·조합은 구조 참고용이며, 색·로고·브랜드 요소는 항상 시디즈 정본이 우선한다.
- 반응형(모바일/태블릿) 브레이크포인트는 화면 예시가 PC 기준이라 미정 → `[확인 필요]`.
