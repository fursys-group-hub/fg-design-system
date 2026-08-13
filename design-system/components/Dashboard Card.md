# Dashboard Card

- **노드 ID:** `69:8975` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Dashboard Card | W×H 314×65, padding(TRBL) 16/20/16/20, radius 4 | Caption/Caption1-SemiBold, Title/Title3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 고정/교차 hug · gap 0

## 하위 구조 (대표 variant, 2~3레벨)

`Dashboard Card` — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 고정/교차 hug · gap 0
- Tag (instance) [레이아웃 가로(H) · 가로 hug/세로 고정] · → State=Light, Color=Black
  - 태그 (text) [가로 hug/세로 hug] · 텍스트 Caption/Caption1-SemiBold
- Frame 4192 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · grow 1.0]
  - 100 (text) [가로 hug/세로 hug] · 텍스트 Title/Title3-SemiBold
  - Frame 1000007756 (frame) [레이아웃 세로(V) · 가로 고정/세로 hug]
    - 건 (text) [가로 fill/세로 hug · stretch] · 텍스트 Caption/Caption1-SemiBold

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

