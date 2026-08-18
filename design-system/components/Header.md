# Header

- **노드 ID:** `68:4651` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Header | W×H 1344×50, padding(TRBL) -/24/-/24 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000), Red-600 (#FF3A4A), #FEFEFE, Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7) | Caption/Caption2-SemiBold, Body/Body1-SemiBold, Caption/Caption1-SemiBold | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 10는 최소 간격)

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Header` — 배경 **Grey-50 (#FFFFFF)** · 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 10는 최소 간격)
- Icon / PanelLeft (instance) [가로 고정/세로 고정 · 크기 20×20] · → Icon / PanelLeft
  - Vector (vector) [크기 15×15] · 선 Grey-900 (#000000)
- Frame 1000006988 (frame) [레이아웃 가로(H) · 가로 고정/세로 hug · 크기 703×32]
  - Frame 1000007706 (frame) [가로 고정/세로 고정 · 크기 20×20]
    - Icon / Bell (instance) [크기 20×20] · → Icon / Bell
    - textBadge (instance) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 16×15] · 배경 Red-600 (#FF3A4A), → Color=Error, Shape=Round, Size=S
  - Frame 1000007718 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 147×32] · 배경 Grey-50 (#FFFFFF), 선 Grey-200 (#EAEDF0)
    - Frame 1000007734 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 99×20]
    - Icon / ChevronDown (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / ChevronDown

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

