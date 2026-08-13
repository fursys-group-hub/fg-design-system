# Header

- **노드 ID:** `68:4651` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Header | W×H 1344×50, padding(TRBL) -/24/-/24 | Body/Body1-SemiBold, Caption/Caption1-SemiBold, Caption/Caption2-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), #FEFEFE, Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · sizing 주축 고정/교차 고정 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 10는 최소 간격)

## 하위 구조 (대표 variant, 2~3레벨)

`Header` — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · sizing 주축 고정/교차 고정 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 10는 최소 간격)
- Icon / PanelLeft (instance) [가로 고정/세로 고정] · → Icon / PanelLeft
  - Vector (vector)
- Frame 1000006988 (frame) [레이아웃 가로(H) · 가로 고정/세로 hug]
  - Frame 1000007706 (frame) [가로 고정/세로 고정]
    - Icon / Bell (instance) · → Icon / Bell
    - textBadge (instance) [레이아웃 가로(H) · 가로 hug/세로 hug] · → Color=Error, Shape=Round, Size=S
  - Frame 1000007718 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
    - Frame 1000007734 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
    - Icon / ChevronDown (instance) [가로 고정/세로 고정] · → Icon / ChevronDown

## 연결된 시맨틱 FILL 스타일

- `Main colors/Main Gray/main-gray_50`

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

