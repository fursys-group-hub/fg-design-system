<!-- 자동 생성 파일 — 원본은 design-system/. 직접 수정 금지. -->
> **버전: 2026-08-18 / 생성 커밋: `f25b38f`**
> 자동 생성 파일 — 원본은 `design-system/`. 직접 수정 금지. 정본 덤프 lastModified: 2026-08-13T07:54:52Z.
> **이 문서는 값·규격.** 화면 조립=`design-principles.md` · 아이콘=`icons.md` · 레이아웃(화면 유형·치수)=`layouts.md` 참조.

# SIDIZ 디자인 시스템 — 배포본

> **자동 생성 파일입니다.** 원본(source of truth)은 저장소의 `design-system/`이며, 이 문서는 그것을 실무용으로 통합·가공한 배포물입니다. 값 수정은 정본에서 하고 다시 export 하세요. (정본 → 배포물 단방향)

AI/실무자가 이 문서만 읽고 SIDIZ 규격대로 화면을 만들 수 있도록 **값 + 사용 규칙**을 함께 싣습니다. 스타일은 함께 배포된 `tokens.css`의 CSS 변수·클래스로 적용하세요.

---

## 0. 개요 · 핵심 원칙

- **폰트:** Pretendard 단일. 모든 텍스트 `line-height: 150%`, `letter-spacing: 1%(0.01em)`.
- **브랜드 포인트 색:** `Blue-700 #003EFF` — 강조/선택/링크에만 **절제** 사용. 남용 금지.
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

용도: Blue-700이 브랜드 포인트. System(Red)은 에러·경고 전용. Grey는 기반 무채색.

### Primary (Blue)
| 토큰 | 값 | CSS 변수 | 용도·규칙 |
|---|---|---|---|
| Blue-700 | `#003EFF` | `--sidiz-color-blue-700` | 브랜드 포인트(강조/선택/링크). 남용 금지 |
| Blue-500 | `#357FFF` | `--sidiz-color-blue-500` | 보조/hover |
| Blue-100 | `#E3EDFF` | `--sidiz-color-blue-100` | 선택·활성 **배경**(연한 파랑) |

### System (Red)
| 토큰 | 값 | CSS 변수 | 용도·규칙 |
|---|---|---|---|
| Red-600 | `#FF3A4A` | `--sidiz-color-red-600` | 에러·경고 텍스트/보더 |
| Red-100 | `#FFECEE` | `--sidiz-color-red-100` | 에러 **배경**(연한) |

### Grey (10단계)
| 토큰 | 값 | CSS 변수 |
|---|---|---|
| Grey-900 | `#000000` | `--sidiz-color-grey-900` |
| Grey-800 | `#242526` | `--sidiz-color-grey-800` |
| Grey-700 | `#434548` | `--sidiz-color-grey-700` |
| Grey-600 | `#595C5E` | `--sidiz-color-grey-600` |
| Grey-500 | `#7C8084` | `--sidiz-color-grey-500` |
| Grey-400 | `#A4AAB0` | `--sidiz-color-grey-400` |
| Grey-300 | `#D6DADE` | `--sidiz-color-grey-300` |
| Grey-200 | `#EAEDF0` | `--sidiz-color-grey-200` |
| Grey-100 | `#F5F6F7` | `--sidiz-color-grey-100` |
| Grey-50 | `#FFFFFF` | `--sidiz-color-grey-50` |

### 컴포넌트 로컬 색 (변수화 제외 — 지정 컴포넌트 한정)
저빈도로 의도적으로 전역 토큰에서 제외한 색. **아래 지정 컴포넌트에서만** 사용하고, 다른 곳에서는 쓰지 않는다.

| 값 | 사용 컴포넌트 | 용도 |
|---|---|---|
| `#38BA77` | Tag (Color=Green) | Green 태그 전경 |
| `#E7F6E7` | Tag (Color=Green, Light) | Green 태그 배경 |
| `#E8C32E` | Tag (Color=Yellow) | Yellow 태그 전경 |
| `#FCF7DF` | Tag (Color=Yellow, Light) | Yellow 태그 배경 |
| `#F5CA1D` | Toast (State=Alert) | Alert 토스트 경고 아이콘 |

> **로고 전용:** `#1D1D1B`는 Signature 로고 아트워크 색으로, UI(텍스트·배경·보더)에는 쓰지 않는다.
> 그 밖의 팔레트 밖 색(그라데이션·보라 등)은 정본이 아닙니다. 사용하지 마세요.

---

## 2. 타이포그래피

Pretendard 단일 · LH 150% · LS 1%(0.01em) 공통. 14종. `tokens.css`의 조합 클래스(`.title1`~`.caption5`)로 적용.

| 토큰(별칭) | Size | Weight | 클래스 | 용도 |
|---|---|---|---|---|
| Title1 | 40px | 600 | `.title1` | 프로모션 대제목 |
| Title2 | 26px | 600 | `.title2` | 프로모션 중제목 |
| Title3 | 22px | 600 | `.title3` | 페이지 메인 타이틀 |
| Title4 | 16px | 600 | `.title4` | 섹션 타이틀 |
| Title5 | 14px | 600 | `.title5` | Card/Modal 타이틀 |
| Body1 | 13px | 600 | `.body1` | 그룹 타이틀 |
| Body2 | 13px | 400 | `.body2` | 그룹 타이틀 보조 |
| Body3 | 12px | 600 | `.body3` | 본문 강조 |
| Body4 | 12px | 400 | `.body4` | 기본 본문 |
| Caption1 | 11px | 600 | `.caption1` | Label, 헬프 텍스트 |
| Caption2 | 10px | 600 | `.caption2` | 뱃지·태그 텍스트 |
| Caption3 | 10px | 400 | `.caption3` | 서브 문구 |
| Caption4 | 8px | 600 | `.caption4` | 최소 표기 강조(뱃지/라벨 전용) |
| Caption5 | 8px | 400 | `.caption5` | 최소 표기(뱃지/라벨 전용) |

> **최소 크기 규칙:** Caption4·5(8·10px)는 본문에 쓰지 않는다.

---

## 3. 스페이싱 · Radius

컴포넌트 변수 바인딩 값에서 집계한 실사용 스케일. (변수 토큰명은 정본에서 `[확인 필요]` — 값은 확정)

### Padding / Gap 스케일 (`--sidiz-space-{n}`)
`2 · 4 · 5 · 6 · 8 · 10 · 12 · 16 · 20 · 24 · 32 · 40 · 64 · 80 · 100` (px)
- 주력은 **8·12px**. 큰 값(64·80)은 섹션/레이아웃 여백.

### Corner Radius (`--sidiz-radius-{n}`)
`2 · 4 · 5 · 6 · 32 · 40 · 9999` (px)
- 버튼/인풋 기본 **4·6**, 큰 곡률 32·40, `9999`=pill(태그/칩/원형).

---

## 4. 이펙트 (그림자)

기본은 border 구분. 그림자는 떠 있는 표면에만.

| 토큰 | CSS 변수 | 값 | 용도 |
|---|---|---|---|
| Drop Shadow | `--sidiz-shadow-dropshadow` | `0 4px 6px -2px #000000@0.05, 0 10px 15px -3px #000000@0.10` (2겹) | 팝오버/드롭다운/카드/토스트 부양 |
| shadow/sm | `--sidiz-shadow-sm` | `0 1px 2px 0 #000000@0.05` | 미세 상승(입력/작은 요소) |

---

## 5. 컴포넌트 명세 (19)

각 컴포넌트는 정본 variant 목록·크기·적용 토큰 기준. 색/간격은 Figma 변수 바인딩(값 확정, 변수명 미제공).

### 컴포넌트 오토레이아웃 요약 (배치 필수 정보)

렌더링 시 방향·정렬을 반드시 지킨다. **`SPACE_BETWEEN`=자식을 양끝으로 밀어 배치**(고정 gap 아님). 상세 하위 구조는 정본 `components/*.md`.

| 컴포넌트 | 방향 | 정렬(주축·교차) |
|---|---|---|
| Button | 가로 | 주축 가운데 · 교차 가운데 |
| Input | 가로 | 주축 시작 · 교차 가운데 |
| Input Case | 세로 | 주축 시작 · 교차 시작 |
| Checkbox / Radio | 없음(자유배치) | — |
| Dropdown List | 세로 | 주축 시작 · 교차 시작 |
| Search Filter | 세로 | 주축 끝 · 교차 끝 |
| Tab | 가로 | 주축 시작 · 교차 시작 |
| Tag | 가로 | 주축 가운데 · 교차 가운데 |
| Table Cell | 가로 | 주축 시작 · 교차 가운데 |
| **Toast Popup** | 가로 | **주축 양끝(SPACE_BETWEEN)** · 교차 가운데 |
| Carousel | 가로 | 주축 가운데 · 교차 가운데 |
| Sidebar | 세로 | 주축 시작 · 교차 시작 |
| Breadcrumb | 가로 | 주축 시작 · 교차 가운데 |
| Dashboard Card | 가로 | 주축 시작 · 교차 가운데 |
| **Header** | 가로 | **주축 양끝(SPACE_BETWEEN)** · 교차 가운데 |
| Pagination | 가로 | 주축 시작 · 교차 가운데 |

### 5.1 Button — 12 variant
- **속성:** Varient(Primary/Secondary/Disabled/Error) × Shape(Square/Round/Text/Flat)
- **크기:** 대부분 H32, Flat은 H24. radius: Square=4, Round/Text/Flat=9999, gap 8, padding 좌우 12(Flat 10).
- **텍스트:** Round/Square=Body1(13/600), Text/Flat=Body3(12/600).
- **색 규칙:** Primary=Grey-900 배경/텍스트 강조, Secondary=Grey-900+Grey-200 보더, Disabled=Grey-400/Grey-200, Error=Red-600.
- **사용 규칙:** 한 화면의 "결정 버튼"은 하나. 파란 채움 버튼을 기본으로 쓰지 않는다.

### 5.2 Input — 28 variant
- **속성:** Varient(Text/Search/Date/Stepper/Unit/Composite/Dropdown) × State(Default/Hover/Filled/Disabled)
- **크기:** H36, radius 4, padding 8/12. 텍스트 Body2(13/400).
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

### 5.8 Tab — 2 variant
- **속성:** Varient(Box/Line). H40, 텍스트 Title5(14/600), **shadow/sm**.
- Line 탭 활성 밑줄 **Blue-700**. **사용 규칙:** 선택 탭만 포인트 색.

### 5.9 Tag — 12 variant
- **속성:** State(Light/Dark) × Color(Red/Green/Blue/Gray/Yellow/Black). 28×16, padding 좌우 4, **radius 2**, 텍스트 Caption1(11/600).
- 정본 팔레트 매핑: Blue=Blue-500/Blue-100, Red=Red-600/Red-100, Gray=Grey-400/Grey-100, Black=Grey-900.
- **컴포넌트 로컬 색:** Green(`#38BA77`/`#E7F6E7`)·Yellow(`#E8C32E`/`#FCF7DF`)는 Tag 전용 로컬 색(전역 토큰 아님). Tag 밖에서 사용 금지. (1장 "컴포넌트 로컬 색" 참조)

### 5.10 Table Cell — 13 variant
- **속성:** Varient(Header/Cell) × Type(Checkbox/Text/Link/Textlink/Radio/Icon/Button/Tag/Calendar/Input). H32(Header)/H38(Cell), padding 좌우 16.
- Header 텍스트 Caption1, Cell 텍스트 Body2(Button 셀=Body3). 보더 Grey-200/Grey-300.
- **사용 규칙:** 표는 셀 타입 조합으로 구성. 구분은 hairline(Grey-200).

### 5.11 Toast Popup — 3 variant
- **속성:** State(Default/Error/Alert). W520×H56, padding 12/32, radius 6, **Drop Shadow**.
- Default 포인트 Blue-500, Error Red-600, Alert 노랑(`#F5CA1D`, Toast 전용 로컬 색). 텍스트 Body1+Body2.
- **레이아웃:** 가로 auto-layout, **주축 SPACE_BETWEEN**(왼쪽 콘텐츠[아이콘+텍스트] / 오른쪽 Button 인스턴스를 양끝 배치 — 고정 gap 아님).
- **사용 규칙:** 떠 있는 알림 → 그림자. 상태색은 아이콘/포인트에만.

### 5.12 Carousel — 2 variant
- **속성:** Varient(Indicator/Navigator). Indicator=점 6px(Grey-50 + 30% 투명), Navigator=80×30(Grey-50 70% 투명 배경).

### 5.13 Sidebar — 4 variant
- **속성:** Varient(Favorite/Default) × States(Default/Extended/Hover). W256×H1080, padding 좌우 12, gap 24, **shadow/sm**.
- 텍스트 Body1 + Title5(그룹 타이틀). Hover 활성 항목 **Blue-700** + 배경 Blue-100.
- **로고:** 상단 브랜드 심볼은 **[§6 로고 SVG](#6-로고-svg-attention-심볼)(Attention)** 를 사용한다. Lucide 등 아이콘 세트로 대체 금지.
- **사용 규칙:** 흰 배경 사이드바. 활성 메뉴만 포인트 색.

### 5.14 Breadcrumb — 1
- W308×H20, gap 8. 텍스트 Body1(현재)/Body2. 구분자 ChevronRight 아이콘. 현재 위치 Grey-900, 상위 Grey-400.
- **사용 규칙:** `·`/`•` 대신 chevron 아이콘 사용.

### 5.15 Dashboard Card — 1
- W314×H65, padding 16/20, radius 4, 보더 Grey-200. 텍스트 Title3(수치)+Caption1(라벨). Tag 포함.
- **사용 규칙:** 그림자 없이 border로 구분. 수치는 Title3, 라벨은 Caption1.

### 5.16 Header — 1
- W1344×H50, padding 좌우 24, gap 10. 텍스트 Body1/Caption1/Caption2. 보더 하단 Grey-200.
- **사용 규칙:** 흰색 헤더(다크/네이비 금지). 심볼 마크는 **[§6 로고 SVG](#6-로고-svg-attention-심볼)** 사용(아이콘 세트 대체 금지).

### 5.17 Pagination — 1
- W176×H20, gap 12. 텍스트 Body1(현재)/Body2. Chevron 좌우 아이콘. 현재 페이지 Grey-900.

### 5.18 Attention (로고) — 2 variant
- **속성:** Sort=Attention × Color(Black/White). 60×84. Black=Grey-900, White=Grey-50.
- 인라인 SVG는 **[§6 로고 SVG](#6-로고-svg-attention-심볼)** 참조. 브랜드 심볼로 이 SVG만 사용(아이콘 대체 금지).

### 5.19 Signature (로고) — 2 variant
- **속성:** Sort=Signature × Color(Black/White). 200×59.
- **사용 규칙:** 심볼/시그니처 로고 사용, "SIDIZ" 워드마크 텍스트 금지.

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

> 로고는 형태 변형 금지. "SIDIZ" 워드마크 텍스트로 대체하지 마세요.

---

## 참고

- 정본 컴포넌트별 전체 variant 행(크기·색 상세)은 저장소 `design-system/components/*.md`에 있습니다.
- 이 배포본은 정본을 압축한 요약이며, 값 불일치 시 **정본이 우선**합니다.
