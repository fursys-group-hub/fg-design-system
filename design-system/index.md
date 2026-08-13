# SIDIZ 디자인 시스템 — 라우터 (index)

이 폴더(`design-system/`)는 SIDIZ 디자인의 **원본 기준서(source of truth)** 이며, 이 `index.md`는 **라우터**다.

> **이 파일의 목적:** 스킬/에이전트는 디자인 작업 전에 **이 index.md만 먼저 읽고**, 아래 매핑표에서 작업 유형에 맞는 문서만 골라 로드한다. 전체 문서를 다 읽지 말고, 필요한 것만 선택적으로 로드한다.

- 값의 최종 원본은 Figma `시디즈_디자인 시스템` (`figma.com/design/UsCx1wPybDpRRBglYY5Nmx`), 로컬 덤프 `sources/figma-raw.json`.
- 이 폴더 문서는 Figma 값을 옮긴 기준서다. `tokens.css` 등 코드 파일은 여기서 변환해 만들며 지금은 만들지 않는다.

---

## 작업 유형별 → 읽을 문서 (라우팅표)

| 작업 유형 | 먼저 읽을 문서 |
|---|---|
| 색상·팔레트·브랜드 컬러 | [tokens/color.md](tokens/color.md) |
| 폰트·텍스트·타이포·크기·굵기 | [tokens/typography.md](tokens/typography.md) |
| 여백·간격·padding·gap·radius·그리드 | [tokens/spacing.md](tokens/spacing.md) |
| 그림자·elevation·떠있는 표면 | [tokens/effect.md](tokens/effect.md) |
| 버튼 | [components/Button.md](components/Button.md) |
| 입력창·폼 필드 | [components/Input.md](components/Input.md), [Input Case](components/Input%20Case.md) |
| 체크박스·라디오·선택 컨트롤 | [Checkbox](components/Checkbox.md), [Radio](components/Radio.md) |
| 드롭다운·셀렉트·메뉴 | [Dropdown List](components/Dropdown%20List.md) |
| 검색·필터 | [Search Filter](components/Search%20Filter.md) |
| 탭·사이드바·헤더·브레드크럼·페이지네이션 (내비) | [Tab](components/Tab.md), [Sidebar](components/Sidebar.md), [Header](components/Header.md), [Breadcrumb](components/Breadcrumb.md), [Pagination](components/Pagination.md) |
| 태그·뱃지·칩 | [Tag](components/Tag.md) |
| 테이블·표·셀 | [Table Cell](components/Table%20Cell.md) |
| 카드·대시보드 위젯 | [Dashboard Card](components/Dashboard%20Card.md) |
| 토스트·알림·스낵바 | [Toast Popup](components/Toast%20Popup.md) |
| 캐러셀·슬라이더 | [Carousel](components/Carousel.md) |
| 로고 | [Attention](components/Attention.md), [Signature](components/Signature.md) |
| 아이콘·아이콘 세트 | [icons.md](icons.md) |
| 화면 조립·레이아웃·화면 유형(목록/상세/대시보드/모달/인증) | [layouts.md](layouts.md) |
| 새 화면 전체·프로토타입 | **tokens 4종 전부** + [icons.md](icons.md) + [layouts.md](layouts.md) + 해당 컴포넌트 문서 |

---

## 토큰 문서 (4)

| 문서 | 한 줄 설명 |
|---|---|
| [tokens/color.md](tokens/color.md) | Foundation 팔레트 — Primary(Blue) / System(Red) / Grey 10단계. 브랜드 `Blue-700 #003EFF`. |
| [tokens/typography.md](tokens/typography.md) | Pretendard 단일, Title1~5 / Body1~4 / Caption1~5 (LH 150% · LS 1%). 스타일명+별칭+용도. |
| [tokens/spacing.md](tokens/spacing.md) | 컴포넌트 변수에서 집계한 radius / padding / gap 스케일. |
| [tokens/effect.md](tokens/effect.md) | 그림자 2종(Drop Shadow, shadow/sm). 기본은 border, 그림자는 떠있는 표면만. |

## 컴포넌트 문서 (19)

| 문서 | 한 줄 설명 |
|---|---|
| [Button](components/Button.md) | 버튼 — Varient(Primary/Secondary/Disabled/Error) × Shape(Square/Round/Text/Flat), 12 variant. |
| [Input](components/Input.md) | 입력 필드 — 상태·타입 조합 28 variant. |
| [Input Case](components/Input%20Case.md) | 입력 필드 케이스(라벨/헬프/에러 등 조합 래퍼). |
| [Checkbox](components/Checkbox.md) | 체크박스 — 5 variant. |
| [Radio](components/Radio.md) | 라디오 버튼 — 3 variant. |
| [Dropdown List](components/Dropdown%20List.md) | 드롭다운 목록/메뉴 — 5 variant. |
| [Search Filter](components/Search%20Filter.md) | 검색 필터 바 — Default/Extended. |
| [Tab](components/Tab.md) | 탭 내비게이션. |
| [Tag](components/Tag.md) | 태그/칩 — 12 variant. |
| [Table Cell](components/Table%20Cell.md) | 테이블 셀 — 텍스트/체크/캘린더 등 13 variant. |
| [Toast Popup](components/Toast%20Popup.md) | 토스트 알림 — 3 variant. |
| [Carousel](components/Carousel.md) | 캐러셀/슬라이더. |
| [Sidebar](components/Sidebar.md) | 좌측 사이드바 내비 — All/Favorite. |
| [Breadcrumb](components/Breadcrumb.md) | 브레드크럼 경로. |
| [Dashboard Card](components/Dashboard%20Card.md) | 대시보드 카드 위젯. |
| [Header](components/Header.md) | 상단 헤더 바. |
| [Pagination](components/Pagination.md) | 페이지네이션. |
| [Attention](components/Attention.md) | Attention 로고. |
| [Signature](components/Signature.md) | Signature 로고. |

## 자산·조립 문서

| 문서 | 한 줄 설명 |
|---|---|
| [icons.md](icons.md) | Lucide 아이콘 세트(24×24·2px)·이름 규칙·컴포넌트별 사용 아이콘 매핑. |
| [layouts.md](layouts.md) | 화면 유형별 골격·공통 치수(사이드바 256·헤더 50 등)·컴포넌트 조합 규칙. |
| [design-principles.md](design-principles.md) | 화면 조립·판단 원칙(레이아웃·위계·패턴). `/sync` 대상 아님(관리자 직접 수정). |

기타: [extraction-plan.md](extraction-plan.md) — 추출 체크리스트·진행 로그(작업 이력용, 디자인 작업 시 필독 아님).

---

## 작성 원칙

세부 원칙은 저장소 루트 `CLAUDE.md`의 "디자인 시스템 문서 작성 원칙"을 따른다. 요약:

- 토큰 형식: **토큰 이름 / 값 / 용도 / 사용 규칙**
- 못 읽었거나 불확실한 값은 **추측하지 말고 `[확인 필요]`** 로 남긴다.
- 문서 1개는 **500줄 이내**. 넘으면 분할한다.
