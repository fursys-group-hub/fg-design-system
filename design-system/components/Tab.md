# Tab

- **노드 ID:** `66:2256` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Box, Line

## Variant 전체 (2)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Line | W×H 570×40 | Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-300 (#D6DADE), Grey-50 (#FFFFFF) | Blue-700 (#003EFF), #18181B, #71717A, Grey-200 (#EAEDF0) | shadow/sm |
| Varient=Box | W×H 608×40 | Body/Body2-Regular, Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | #18181B, #71717A | shadow/sm |

## 레이아웃 (오토레이아웃)

- **Varient=Line**: 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 0
- **Varient=Box**: 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 0

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Line` — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 0
- Select (frame) [레이아웃 가로(H) · 가로 hug/세로 고정]
  - Icon / Sun (instance) [가로 고정/세로 고정] · → Icon / Sun
    - Vector (vector)
  - 선택 메뉴명 (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
  - 100 (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정] · → Icon / Sun
    - Vector (vector)
  - Tabs Text (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정] · → Icon / Sun
    - Vector (vector)
  - Tabs Text (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정] · → Icon / Sun
    - Vector (vector)
  - Tabs Text (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정] · → Icon / Sun
    - Vector (vector)
  - Tabs Text (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Box / Line) 변화 시 → 달라짐: **fill, stroke, 레이아웃, 크기, 텍스트** · 동일: 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

