# Sidebar

- **노드 ID:** `69:5382` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Favorite, Default
- **States**: Default, Extended, Hover

## Variant 전체 (4)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Favorite, States=Default | W×H 256×1080, padding(TRBL) -/12/-/12 | Body/Body1-SemiBold, Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0), #ECECEC | shadow/sm |
| Varient=Default, States=Extended | W×H 256×1080, padding(TRBL) -/12/-/12 | Body/Body1-SemiBold, Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0), #ECECEC | shadow/sm |
| Varient=Default, States=Hover | W×H 256×1080, padding(TRBL) -/12/-/12 | Body/Body1-SemiBold, Title/Title5-SemiBold | Grey-900 (#000000), Blue-700 (#003EFF), Grey-400 (#A4AAB0), Blue-100 (#E3EDFF), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Blue-700 (#003EFF), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0), #ECECEC | shadow/sm |
| Varient=Default, States=Default | W×H 256×1080, padding(TRBL) -/12/-/12 | Body/Body1-SemiBold, Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0), #ECECEC | shadow/sm |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 고정/교차 고정 · gap 24

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Favorite, States=Default` — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 고정/교차 고정 · gap 24
- Frame 1000007000 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
  - Frame 1000007777 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
    - Attention (instance) [가로 고정/세로 고정] · → Sort=Attention, Color=Black
    - (시스템명) (text) [가로 hug/세로 hug] · 텍스트 Title/Title5-SemiBold
  - Search (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]
    - Icon / Search (instance) [가로 고정/세로 고정] · → Icon / Search
    - PlaceholderText (text) [가로 fill/세로 hug · grow 1.0] · 텍스트 Body/Body1-SemiBold
- Frame 1000007001 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
  - Tab (frame) [레이아웃 세로(V) · 가로 hug/세로 hug]
    - Menu (frame) [레이아웃 가로(H) · 가로 hug/세로 고정]
  - List (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]
    - Sidebar / SidebarMenuItem (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · stretch]

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Default / Favorite) 변화 시 → 달라짐: **없음(동일 형태, 조합만 다름)** · 동일: 크기, 레이아웃, 텍스트, fill, stroke, 이펙트
- **States** (Default / Extended / Hover) 변화 시 → 달라짐: **fill, stroke** · 동일: 크기, 레이아웃, 텍스트, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

