<!-- 배포물(관리자 수기 유지) — 원본(정본)은 design-system/. 실무자 직접 수정 금지. 갱신은 관리자가 정본과 함께 손으로 한다(옛 /export 자동 생성은 폐기). -->
> **버전: 2026-08-31 / 생성 커밋: `4bad7b8`**
> ⚠️ **v6 정본 우선:** 마크업=`COMPONENTS.html`, CSS=`fg-components.css`, 값 규칙=`CLAUDE.md`, 수치 근거=`component-spec.md`. 이 문서와 값이 다르면 그쪽을 따른다.
> 배포물(관리자 수기 유지) — 원본(정본)은 `design-system/`. 실무자 직접 수정 금지(갱신은 관리자가 정본과 함께). 정본 덤프 lastModified: 2026-08-13T07:54:52Z.
> **이 문서는 값·규격.** 화면 조립=`design-principles.md` · 아이콘=`icons.md` · 레이아웃(화면 유형·치수)=`layouts.md` 참조.

# 퍼시스그룹 디자인 시스템 — 배포본

> **배포물입니다.** 원본(source of truth)은 저장소의 `design-system/`이며, 이 문서는 그것을 실무용으로 통합·가공한 것입니다. 값 수정은 **관리자가 정본과 이 배포물을 함께 손으로** 갱신합니다(옛 `/export` 자동 생성은 폐기). 실무자는 직접 수정하지 마세요.

AI/실무자가 이 문서만 읽고 퍼시스그룹 디자인 시스템 규격대로 화면을 만들 수 있도록 **값 + 사용 규칙**을 함께 싣습니다. 스타일은 함께 배포된 `tokens.css`의 CSS 변수·클래스로 적용하세요.

---

## 0. 개요 · 핵심 원칙

> ### ⚠️ 절대 원칙 (예외 없음)
> 시디즈 정본은 **컬러 22색(Primary 2톤·브랜드별 / System 10·공통 / Grey Scale 10·공통) + 타이포 17종(Title1~8, Body1~4, Caption1~5)**뿐이다. Primary 는 9개 브랜드마다 다르다.
> - 이 밖의 색·크기·굵기는 **존재하지 않는다.** 발견되면 오류이자 정본 토큰 교정 대상이다.
> - **신규·근사·중간·예외 토큰 생성 금지. 팔레트 확장 금지.**
> - **화면 제작 시 `tokens.css`의 클래스(타이포 17종 + 컴포넌트 클래스)만 사용한다. `font-size`·`padding`·`height` 등을 직접 지정하지 않는다.** 필요한 클래스가 없으면 임의로 만들지 말고 관리자에게 알린다.
> - 옛 컴포넌트 로컬 확장색(Tag Green/Yellow·Toast Alert)은 **System(Green/Yellow)으로 편입**되어 더 이상 예외가 아니다. 초록=`Green-600/100`, 노랑=`Yellow-600/100`.

- **폰트:** Pretendard 단일. 모든 텍스트 `line-height: 150%`, `letter-spacing: 1%(0.01em)`.
- **브랜드 포인트 색:** `Primary-600`(브랜드별, 기본 그룹사 `#6725F3`) — 강조/선택/링크/건수에만 **절제** 사용. 남용 금지. 브랜드 전환은 `<html data-brand="...">`.
- **무채색 기반:** Grey 10단계(50=흰색 ~ 900=검정)로 텍스트·보더·배경 구성. 임의 회색 발명 금지.
- **구분은 border 우선.** 그림자는 떠 있는 표면(팝오버/드롭다운/토스트)에만.
- **radius:** 버튼/인풋 4~6px, pill(태그/칩/원형) `9999`. 임의값 금지.
- **최소 크기 규칙:** Caption4·5(8·10px)는 **뱃지/태그/아이콘 라벨 전용**, 본문 사용 금지.
- **토큰만 사용:** 아래 팔레트/타이포/스페이싱 밖의 임의 hex·크기·radius를 만들지 않는다.

### 웹폰트 로드 (필수)
HTML을 생성할 때 `<head>`에 아래 한 줄을 넣고 `body`에 폰트를 지정하세요. (Pretendard 미로드 시 규격이 깨집니다.)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css">
```
```css
body { font-family: 'Pretendard', sans-serif; }
```

---

## 1. 컬러

용도: Primary(브랜드별 2톤)가 브랜드 포인트. System 10은 상태 색(완료/진행중/보류/취소·에러). Grey는 기반 무채색. 총 **22색**.

### Primary (브랜드별 · 2톤 · 기본 그룹사 공통)
`<html data-brand="...">` 로 전환. 600=브랜드 포인트(버튼 배경·사이드바 활성·라인탭 밑줄·섹션 건수), 200=사이드바 활성 배경.

| 토큰 | CSS 변수 | 용도·규칙 |
|---|---|---|
| Primary-600 | `--fg-color-primary-600` | 브랜드 포인트. 강조/선택/링크/건수에만 절제 사용 |
| Primary-200 | `--fg-color-primary-200` | 브랜드 강조 **배경**(사이드바 활성 배경) |

**브랜드별 값(9):** 시디즈 `#003EFF`/`#E3EDFF` · 퍼시스 `#E3001C`/`#FCE5E8` · 일룸 `#D60707`/`#FEDADA` · 데스커 `#272727`/`#E9E9E9` · 알로소 `#000000`/`#E9E9E9` · 슬로우베드 `#0D207C`/`#D7E4F0` · 레터스 `#FF5C39`/`#FFF3ED` · 퍼플식스 `#7800F5`/`#F4E8FF` · 그룹사 공통(기본) `#6725F3`/`#F0E9FE`

### System (9브랜드 공통 · 각 600/100)
| 토큰 | 값 | CSS 변수 | 용도·규칙 |
|---|---|---|---|
| Red-600 | `#EF2E32` | `--fg-color-red-600` | 취소/실패·에러 텍스트/보더/채움 |
| Red-100 | `#FBE7E7` | `--fg-color-red-100` | 취소/실패·에러 **배경**(연한) |
| Yellow-600 | `#D4A300` | `--fg-color-yellow-600` | 보류 전경/채움 |
| Yellow-100 | `#F9F1D9` | `--fg-color-yellow-100` | 보류 **배경**(연한) |
| Green-600 | `#2AA75E` | `--fg-color-green-600` | 진행중 전경/채움 |
| Green-100 | `#DFF2E7` | `--fg-color-green-100` | 진행중 **배경**(연한) |
| Blue-600 | `#3769DE` | `--fg-color-blue-600` | 완료 전경/채움 |
| Blue-100 | `#EBF0FC` | `--fg-color-blue-100` | 완료 **배경**(연한) |
| Gray-600 | `#909090` | `--fg-color-gray-600` | System 무채 전경(Grey Scale 와 별개) |
| Gray-100 | `#F0F0F0` | `--fg-color-gray-100` | System 무채 배경 |

### Grey (10단계)
| 토큰 | 값 | CSS 변수 |
|---|---|---|
| Grey-900 | `#000000` | `--fg-color-grey-900` |
| Grey-800 | `#242526` | `--fg-color-grey-800` |
| Grey-700 | `#434548` | `--fg-color-grey-700` |
| Grey-600 | `#595C5E` | `--fg-color-grey-600` |
| Grey-500 | `#7C8084` | `--fg-color-grey-500` |
| Grey-400 | `#A4AAB0` | `--fg-color-grey-400` |
| Grey-300 | `#D6DADE` | `--fg-color-grey-300` |
| Grey-200 | `#EAEDF0` | `--fg-color-grey-200` |
| Grey-100 | `#F5F6F7` | `--fg-color-grey-100` |
| Grey-50 | `#FFFFFF` | `--fg-color-grey-50` |

### 컴포넌트 로컬 색 — 폐지 (System 으로 편입)
기존 로컬 확장색(Tag Green/Yellow·Toast Alert)은 **System 색으로 편입**되어 더 이상 로컬 색이 아니다.

| 옛 로컬 색 | 대체 System 토큰 |
|---|---|
| Tag Green `#38BA77`/`#E7F6E7` | `Green-600` `#2AA75E` / `Green-100` `#DFF2E7` |
| Tag Yellow `#E8C32E`/`#FCF7DF` | `Yellow-600` `#D4A300` / `Yellow-100` `#F9F1D9` |
| Toast Alert `#F5CA1D` | `Yellow-600` `#D4A300` |

> **로고 전용:** `#1D1D1B`는 Signature 로고 아트워크 색으로, UI(텍스트·배경·보더)에는 쓰지 않는다.
> 그 밖의 팔레트 밖 색(그라데이션·보라 등)은 정본이 아닙니다. 사용하지 마세요.

---

## 2. 타이포그래피

Pretendard 단일 · LH 150% · LS 1%(0.01em) 공통. 17종. `tokens.css`의 조합 클래스(`.title1`~`.caption5`)로 적용.

| 토큰(별칭) | Size | Weight | 클래스 | 용도 |
|---|---|---|---|---|
| Title1 | 40px | 600 | `.title1` | 프로모션 대제목 |
| Title2 | 32px | 600 | `.title2` | 프로모션 대제목 |
| Title3 | 26px | 600 | `.title3` | 프로모션 중제목 |
| Title4 | 22px | 600 | `.title4` | 페이지 메인 타이틀 |
| Title5 | 16px | 600 | `.title5` | 섹션 타이틀 |
| Title6 | 16px | 400 | `.title6` | 섹션 타이틀 |
| Title7 | 14px | 600 | `.title7` | Card/Modal 타이틀 |
| Title8 | 14px | 400 | `.title8` | Card/Modal 타이틀 |
| Body1 | 13px | 600 | `.body1` | 그룹 타이틀 |
| Body2 | 13px | 400 | `.body2` | 그룹 타이틀 보조 |
| Body3 | 12px | 600 | `.body3` | 본문 강조 |
| Body4 | 12px | 400 | `.body4` | 기본 본문 |
| Caption1 | 11px | 600 | `.caption1` | Label, 헬프 텍스트 |
| Caption2 | 10px | 600 | `.caption2` | 뱃지, 태그 텍스트 |
| Caption3 | 10px | 400 | `.caption3` | 서브 문구 |
| Caption4 | 8px | 600 | `.caption4` | 최소 표기 강조 |
| Caption5 | 8px | 400 | `.caption5` | 최소 표기 |

> **최소 크기 규칙:** Caption4·5(8·10px)는 본문에 쓰지 않는다.

> ⚠️ **동명이값 주의(정본 아님):** 로컬에 정본과 이름이 같으나 값이 다른 구세대 스타일 2종이 잔존해 오선택 위험이 있다. 값을 확인해 피한다.
> - `Body/Body2-Regular` 구세대 = 15px / LH 160% / LS -2% (정본은 13px / 150% / 1%)
> - `Body/Body4-Regular` 구세대 = 13px / LH 120% / LS -2% (정본은 12px / 150% / 1%)

### 모바일 축소 (고객 화면)

고객 화면(랜딩·프로모션)은 모바일(폭 768 이하)에서 큰 제목을 한 단계 줄인다. **모바일용 크기를 새로 만들지 않는다. 정의된 17종 이름 안에서 한 단계 내려간다.** `fg-customer.css` 의 기존 `@media (max-width: 768px)` 에서 `var(--fg-font-size-titleN)` 으로 참조하므로 원본 Title 값이 바뀌면 따라간다.

| 데스크톱 | 모바일 |
|---|---|
| Title1 40px | Title3 26px |
| Title2 32px | Title4 22px |
| Title3 26px | Title4 22px |
| Title4 22px | Title5 16px |
| Title5 16px 이하 | 그대로 |

---

## 3. 스페이싱 · Radius

컴포넌트 변수 바인딩 값에서 집계한 실사용 스케일. (변수 토큰명은 정본에서 `[확인 필요]` — 값은 확정)

### Padding / Gap 스케일 (`--fg-space-{n}`)
`2 · 4 · 5 · 6 · 8 · 10 · 12 · 16 · 20 · 24 · 32 · 40 · 64 · 80 · 100` (px)
- 주력은 **8·12px**. 큰 값(64·80)은 섹션/레이아웃 여백.

### Corner Radius (`--fg-radius-{n}`)
`2 · 4 · 5 · 6 · 32 · 40 · 9999` (px)
- 버튼/인풋 기본 **4·6**, 큰 곡률 32·40, `9999`=pill(태그/칩/원형).

---

## 4. 이펙트 (그림자)

기본은 border 구분. 그림자는 떠 있는 표면에만.

| 토큰 | CSS 변수 | 값 | 용도 |
|---|---|---|---|
| Drop Shadow | `--fg-shadow-dropshadow` | `0 4px 6px -2px #000000@0.05, 0 10px 15px -3px #000000@0.10` (2겹) | 팝오버/드롭다운/카드/토스트 부양 |
| shadow/sm | `--fg-shadow-sm` | `0 1px 2px 0 #000000@0.05` | 미세 상승(입력/작은 요소) |

> **잔존 스타일(정본 아님 — 사용 금지):** Internal Only Canvas의 외부 라이브러리 잔재(Switch·DropdownMenu)에서만 쓰이는 그림자. `tokens.css`에 넣지 않았다.
> - `shadow/md` = `0 2px 4px -1px #000000@0.06, 0 4px 6px -1px #000000@0.10` (2겹)
> - `shadow/lg` = `Drop Shadow`와 동일 값

---

## 5. 컴포넌트 명세 (19)

각 컴포넌트는 정본 variant 목록·크기·적용 토큰 기준. 색/간격은 Figma 변수 바인딩(값 확정, 변수명 미제공).

> **배경색 주의:** 대부분 배경은 흰색(`Grey-50`)이나 **Toast Popup·Tag(Dark)는 배경이 `Grey-900`(다크)** 다. 컴포넌트별 배경·요소별 색·아이콘 px 크기의 정확한 귀속은 정본 `components/*.md`(배경/보더/자식 색·하위 구조)를 따른다.

### 컴포넌트 오토레이아웃 요약 (배치 필수 정보)

렌더링 시 방향·정렬을 반드시 지킨다. **`SPACE_BETWEEN`=자식을 양끝으로 밀어 배치**(고정 gap 아님). 상세 하위 구조는 정본 `components/*.md`.

| 컴포넌트 | 방향 | 정렬(주축·교차) |
|---|---|---|
| Button | 가로 | 주축 가운데 · 교차 가운데 · gap: Round/Square 8, Flat/Text 6 |
| Input | 가로 | Date gap12 / Search·Unit·Dropdown SPACE_BETWEEN / Text gap0·시작 / Stepper gap0·좌패딩12 / Composite gap4 |
| Input Case | 세로 | 주축 시작 · 교차 시작 |
| Checkbox / Radio | 없음(자유배치) | — |
| Dropdown List | 세로 | 주축 시작 · 교차 시작 |
| Search Filter | 세로 | 주축 끝 · 교차 끝 |
| Tab | 가로 | 주축 시작 · 교차 시작 |
| Tag | 가로 | 주축 가운데 · 교차 가운데 |
| Table Cell | 가로 | 주축 시작 · 교차 가운데 · gap: Cell/Text 4, 나머지 12변형 0 |
| **Toast Popup** | 가로 | **주축 양끝(SPACE_BETWEEN)** · 교차 가운데 |
| Carousel | 가로 | 주축 가운데 · 교차 가운데 |
| Sidebar | 세로 | 주축 시작 · 교차 시작 |
| Breadcrumb | 가로 | 주축 시작 · 교차 가운데 |
| Dashboard Card | 가로 | 주축 시작 · 교차 가운데 |
| **Header** | 가로 | **주축 양끝(SPACE_BETWEEN)** · 교차 가운데 |
| Pagination | 가로 | 주축 시작 · 교차 가운데 |

### 5.1 Button — 12 variant
- **속성:** Varient(Primary/Secondary/Disabled/Error) × Shape(Square/Round/Text/Flat)
- **크기:** 대부분 H32, Flat은 H24. radius: Square=4, Round/Text/Flat=9999, padding 좌우 12(Flat 10). **gap: Round/Square 8, Flat/Text 6.**
- **텍스트:** Round/Square=Body1(13/600), Text/Flat=Body3(12/600).
- **색 규칙:** Primary=Grey-900 배경/텍스트 강조, Secondary=Grey-900+Grey-200 보더, Disabled=Grey-400/Grey-200, Error=Red-600.
- **사용 규칙:** 한 화면의 "결정 버튼"은 하나. 파란 채움 버튼을 기본으로 쓰지 않는다.

### 5.2 Input — 28 variant
- **속성:** Varient(Text/Search/Date/Stepper/Unit/Composite/Dropdown) × State(Default/Hover/Filled/Disabled)
- **크기:** H36, radius 4, padding 8/12. 텍스트 Body2(13/400).
- **레이아웃(gap 실측):** Date gap12 / Search·Unit·Dropdown 12종 SPACE_BETWEEN / Text gap0·시작 정렬 / Stepper gap0·좌측 패딩12만 / Composite gap4.
- **색 규칙:** Default 보더 Grey-200, Hover/Filled 보더 Grey-900(활성), Disabled Grey-400/Grey-200.
- **사용 규칙:** 상태별 보더색으로 포커스/입력 상태 표현. 배경은 흰색 기본.

### 5.3 Input Case — 2 variant
- **속성:** Varient(Field/Text) — 라벨/헬프/에러 조합 래퍼.
- Field(W314×H84): 라벨(Body3) + 입력 + 헬프/에러(Body4). Text(W124×H44): 라벨+본문(Body2/Body3).
- **사용 규칙:** 폼 필드의 라벨·헬프·에러 묶음 표준. 에러는 Red-600.

### 5.4 Checkbox — 5 variant
- **속성:** State(Unchecked/Checked/Multiple Checked/Hover/Disabled). 16×16.
- Checked=Grey-900 채움, Unchecked=Grey-300 보더, Hover=Grey-900 보더, Disabled=Grey-300.

### 5.5 Radio — 3 variant
- **속성:** State(Activated/Inactive/Hover). 16×16.
- Activated=Grey-900, Inactive=Grey-300 보더, Hover=Grey-900 보더.

### 5.6 Dropdown List — 5 variant
- **속성:** Varient(Single/Multiple/Profile) × State(Default/Hover). radius 4, **Drop Shadow**(Profile).
- 텍스트 Body2 기본. 항목 Hover 배경 Grey-100.
- **사용 규칙:** 떠 있는 목록이므로 그림자 사용. 선택 항목만 강조.

### 5.7 Search Filter — 2 variant
- **속성:** State(Default H91 / Extended H241). W1280, radius 4, gap 8, padding 상하 16.
- 텍스트 Body1/Body2/Body3/Caption1. **사용 규칙:** 필터 확장 시 Extended.
- **일정(기간) 필드:** 날짜 범위는 **한 줄 유지(nowrap), 줄바꿈 금지** — 좁으면 폭을 늘린다(기간 필드 min-width 348).

### 5.8 Tab — 2 variant
- **속성:** Varient(Box/Line). H40, 텍스트 Title7(14/600), **shadow/sm**.
- Line 탭 활성 밑줄 **Primary-600**. **사용 규칙:** 선택 탭만 포인트 색.

### 5.9 Tag — 12 variant
- **속성:** State(Light/Dark) × Color(Red/Green/Blue/Gray/Yellow/Black). 28×16, padding 좌우 4, **radius 2**, 텍스트 Caption1(11/600).
- 정본 팔레트 매핑: Blue=Blue-600/Blue-100, Red=Red-600/Red-100, Gray=Grey-400/Grey-100, Black=Grey-900.
- **컴포넌트 로컬 색:** Green(`#38BA77`/`#E7F6E7`)·Yellow(`#E8C32E`/`#FCF7DF`)는 Tag 전용 로컬 색(전역 토큰 아님). Tag 밖에서 사용 금지. (1장 "컴포넌트 로컬 색" 참조)
- **상태 태그 매핑:** 5범주(대기 black-light / 보류 yellow-light / 진행중 green-light / 완료 blue-light / 취소·실패 요약카드 red-dark·테이블 red-light)와 **라벨은 업무 용어 그대로**(결제완료→완료 금지), 6번째 색 금지 규칙은 **`CLAUDE.md` 「상태 태그 5범주 매핑」이 정본**이다.

### 5.10 Table Cell — 13 variant
- **속성:** Varient(Header/Cell) × Type(Checkbox/Text/Link/Textlink/Radio/Icon/Button/Tag/Calendar/Input). H32(Header)/H38(Cell), padding 좌우 16.
- Header 텍스트 Caption1, Cell 텍스트 Body2(Button 셀=Body3). 보더 Grey-200/Grey-300. **gap: Cell/Type=Text만 4, 나머지 12변형 0.**
- **No.(번호) 열을 두지 않는다.** 첫 열은 체크박스 열(폭 48). (정본: `CLAUDE.md` Table 구조)
- **테이블 전체를 `Grey-200` 외곽선 + radius 4 로 감싼다**(`fg-table-wrap`), 마지막 행 하단 보더 제거.
- **사용 규칙:** 표는 셀 타입 조합으로 구성. 구분은 hairline(Grey-200). 상세 마크업 정본=`COMPONENTS.html`.

### 5.11 Toast Popup — 3 variant
- **속성:** State(Default/Error/Alert). W520×H56, padding 12/32, radius 6, **Drop Shadow**.
- **배경 = `Grey-900`(#000000) 다크. 텍스트 = 흰색(`Grey-50`).** (밝은 배경 아님 — 주의)
- **구조(SPACE_BETWEEN):** 좌측 = 상태 아이콘(**24×24**) + 메시지(흰색 Body1) / 우측 = **"닫기" 텍스트 버튼(`Grey-400`, `Body2` 13/400)만** — **X·아이콘 넣지 않음**(정본은 버튼 내 아이콘 HIDDEN). CSS: `.toast`/`.toast__body`/`.toast__close`.
- **상태 아이콘(포인트 색):** Default = 파랑 체크(`Blue-600`) · Error = 빨강 X(`Red-600`) · Alert = 노랑 !(`Yellow-600`).
- **금지:** 상태 아이콘 20×20, "닫기"를 `Body3`(12/600)로, 밝은 배경.
- **사용 규칙:** 떠 있는 알림 → 그림자. 상태색은 아이콘에만, 배경은 항상 다크.

### 5.12 Carousel — 2 variant
- **속성:** Varient(Indicator/Navigator). Indicator=점 6px(Grey-50 + 30% 투명), Navigator=80×30(Grey-50 70% 투명 배경).

### 5.13 Sidebar — 4 variant
- **속성:** Varient(Favorite/Default) × States(Default/Extended/Hover). W256×H1080, padding 좌우 12, gap 24, **shadow/sm**.
- **메뉴 항목(SidebarMenuButton) 높이 34**, **검색창 높이 38.** 텍스트 Body1 + Title7(그룹 타이틀). 검색 placeholder `Body1`(`Grey-400`). Hover 활성 항목 **Primary-600** + 배경 Primary-200.
- **로고:** 상단 브랜드 심볼은 **[§6 로고 SVG](#6-로고-svg-attention-심볼)(Attention, 18×25)** + 우측 **시스템명(`Title7`) 필수.** Lucide 등 아이콘 세트로 대체 금지, 시스템명 생략 금지. CSS: `.sidebar`/`.sidebar-item`.
- **사용 규칙:** 흰 배경 사이드바. 활성 메뉴만 포인트 색. **금지:** 항목 높이 40·검색 36·시스템명 누락·placeholder를 Body2로.

### 5.14 Breadcrumb — 1
- W308×H20, gap 8. 텍스트 Body1(현재)/Body2. 구분자 ChevronRight 아이콘. 현재 위치 Grey-900, 상위 Grey-400.
- **사용 규칙:** `·`/`•` 대신 chevron 아이콘 사용.

### 5.15 Dashboard Card — 1
- W314×H65 **고정**, padding 16/20, radius 4, 보더 Grey-200. **내부 가로(HORIZONTAL) auto-layout, gap 0.** CSS: `.dashboard-cards`/`.dashboard-card`.
- **내부 구조(가로 1줄):** `Tag`(상태) + [수치 `Title4` + 단위 `Caption1`]. 수치·라벨을 **세로로 쌓지 않는다.**
- **수치·단위 색 = 카드 태그의 진한 색과 동일**: 카드에 `fg-card--wait/--hold/--progress/--done/--fail` 부여 시 자동(정본: `CLAUDE.md` 상태 태그 5범주 · `fg-components.css`).
- **배열:** 요약 카드는 **가로(HORIZONTAL) 1행**, 카드 간 **gap 8**. 세로(상하) 스택 금지.
- **사용 규칙:** 그림자 없이 border로 구분. **금지:** 카드 내부 세로 스택·3줄 구성·gap≠0·높이 가변(65 초과).

### 5.16 Header — 1
- W1344×H50, padding 좌우 24, gap 10, **SPACE_BETWEEN**. 텍스트 Body1/Caption1/Caption2. 보더 하단 Grey-200. CSS: `.header`/`.header__profile`.
- **알림:** `Icon/Bell`(20×20)에 **알림 뱃지(`Red-600`) 필수.** **프로필:** 이름+`ChevronDown`을 **보더 박스(`Grey-200`)로 감싼다(필수).**
- **사용 규칙:** 흰색 헤더(다크/네이비 금지). 심볼 마크는 **[§6 로고 SVG](#6-로고-svg-attention-심볼)** 사용(아이콘 세트 대체 금지). **금지:** 알림 뱃지·프로필 보더 박스 생략.

### 5.17 Pagination — 1
- W176×H20, gap 12. 텍스트 Body1(현재)/Body2. Chevron 좌우 아이콘. 현재 페이지 Grey-900.

### 5.18 Attention (로고) — 2 variant
- **속성:** Sort=Attention × Color(Black/White). 60×84. Black=Grey-900, White=Grey-50.
- 인라인 SVG는 **[§6 로고 SVG](#6-로고-svg-attention-심볼)** 참조. 브랜드 심볼로 이 SVG만 사용(아이콘 대체 금지).

### 5.19 Signature (로고) — 2 variant
- **속성:** Sort=Signature × Color(Black/White). 200×59.
- **사용 규칙:** 심볼/시그니처 로고 사용, 브랜드명을 워드마크 텍스트로 대체 금지.

---

## 6. 로고 SVG (Attention 심볼)

로고는 아래 인라인 SVG를 그대로 사용하세요. viewBox `60×84.3129` 단일 벡터. **Black**=밝은 배경, **White**=어두운 배경.

**Black:**
```html
<svg width="60" height="84.3129" viewBox="0 0 60 84.3129" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M60 0L0 15.5146V37.2516C0 37.7216 0.30934 38.1321 0.755503 38.2451L45.3896 49.7858L0 61.5289V84.3129L60 68.7983V47.1148C60 46.6449 59.6907 46.2344 59.2445 46.1214L14.5033 34.5509L60 22.7841V0Z" fill="black"/></svg>
```

**White:**
```html
<svg width="60" height="84.3129" viewBox="0 0 60 84.3129" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M60 0L0 15.5146V37.2516C0 37.7216 0.30934 38.1321 0.755503 38.2451L45.3896 49.7858L0 61.5289V84.3129L60 68.7983V47.1148C60 46.6449 59.6907 46.2344 59.2445 46.1214L14.5033 34.5509L60 22.7841V0Z" fill="white"/></svg>
```

> 로고는 형태 변형 금지. 브랜드명을 워드마크 텍스트로 대체하지 마세요.

---

## 참고

- 정본 컴포넌트별 전체 variant 행(크기·색 상세)은 저장소 `design-system/components/*.md`에 있습니다.
- 이 배포본은 정본을 압축한 요약이며, 값 불일치 시 **정본이 우선**합니다.
