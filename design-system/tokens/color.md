# Color — SIDIZ 컬러 토큰

정본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`) → **`2. Foundation` 페이지 Color 프레임**.
Foundation에 없는 published 스타일(`Semantic/*`, `Main colors/Main Gray/*`)은 구 세대 잔존물이므로 이 문서에서 제외한다.

## Primary Colors

*용도:* Blue-700이 브랜드 포인트. 선택/링크/강조에만 절제 사용. Blue-100은 선택·활성 배경.

| 토큰 | 값 | 용도·규칙 |
|---|---|---|
| `Blue-700` | `#003EFF` | 브랜드 포인트(강조/선택/링크). 남용 금지 |
| `Blue-500` | `#357FFF` | 보조/hover 상태 |
| `Blue-100` | `#E3EDFF` | 선택·활성 **배경**(연한 파랑) |

## System Colors

*용도:* 에러·경고 전용. 기능 표기로만 소량 사용.

| 토큰 | 값 | 용도·규칙 |
|---|---|---|
| `Red-600` | `#FF3A4A` | 에러·경고 텍스트/보더 |
| `Red-100` | `#FFECEE` | 에러 **배경**(연한) |

## Grey Scale

*용도:* 텍스트·보더·배경 기반 무채색 10단계. 50=흰색, 900=검정. 임의 회색 발명 금지.

| 토큰 | 값 |
|---|---|
| `Grey-900` | `#000000` |
| `Grey-800` | `#242526` |
| `Grey-700` | `#434548` |
| `Grey-600` | `#595C5E` |
| `Grey-500` | `#7C8084` |
| `Grey-400` | `#A4AAB0` |
| `Grey-300` | `#D6DADE` |
| `Grey-200` | `#EAEDF0` |
| `Grey-100` | `#F5F6F7` |
| `Grey-50` | `#FFFFFF` |

## 컴포넌트 로컬 색 (Component-local — 변수화 제외)

*저빈도로 사용되어 의도적으로 전역 변수/토큰에서 제외한 색(디자이너 확정: 비변수화). 아래 **지정 컴포넌트에서만** 사용하며, 다른 컴포넌트·위치에서 쓰면 위반이다.*

| 토큰(별칭) | 값 | 사용 컴포넌트 (한정) | 용도 |
|---|---|---|---|
| Tag Green | `#38BA77` | **Tag** (Color=Green) | Green 태그 전경(Dark 배경 채움 / Light 글자) |
| Tag Green BG | `#E7F6E7` | **Tag** (Color=Green, State=Light) | Green Light 태그 배경 |
| Tag Yellow | `#E8C32E` | **Tag** (Color=Yellow) | Yellow 태그 전경 |
| Tag Yellow BG | `#FCF7DF` | **Tag** (Color=Yellow, State=Light) | Yellow Light 태그 배경 |
| Alert Yellow | `#F5CA1D` | **Toast** (State=Alert) | Alert 토스트 경고 아이콘 |

> 이 색들은 Figma에서 변수 바인딩 없이 컴포넌트 로컬로 지정됨(의도적 비변수화). **지정 컴포넌트 외 사용 금지.** 신규 화면에서 초록/노랑이 필요하면 먼저 팔레트 확장을 검토한다.
> ⚠️ 2026-08-13 sync: Tag Green `#10C266→#38BA77`, Tag Yellow `#F5CA1D→#E8C32E` 변경. Toast Alert 노랑은 `#F5CA1D` 유지(Tag와 분리됨).

## 로고 자산 색 (Logo asset — UI 색 아님)

*로고 아트워크에만 쓰는 색. **팔레트도 allowlist도 아니며, UI(텍스트·배경·보더)에 사용 금지.***

| 값 | 사용 범위 (한정) | 비고 |
|---|---|---|
| `#1D1D1B` | **Signature 로고 벡터**(`66:3931`~`66:3935`)와 그 인스턴스 | 브랜드 로고 근검정. 이 노드 밖에서 fill로 쓰면 위반 |

> Sidebar 등에서 보이는 `#1D1D1B`는 모두 Signature 로고 인스턴스(`I…;66:3931`)이며, 컴포넌트 고유 색이 아니다.

## 가이드/문서 색 (Figma 정리용 — 검사 제외)

*디자인 색이 아니라 Figma 편집·문서 정리용 색. 정본 토큰 아님. design-qa는 위치 무관 **검사 제외**하고 제외 건수만 집계한다.*

- `#8A38F5` — 컴포넌트 세트/인스턴스 표시 테두리
- `#9747FF` — 이미지 플레이스홀더 기본색
- `#F9F4FF` — 로고 전시/정리용 배경(로고 배경 아님)
