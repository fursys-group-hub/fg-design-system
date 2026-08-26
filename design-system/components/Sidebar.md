> ⚠️ 이 파일은 피그마 실측 기록이다. 색 이름은 2026-08-26 구조 개편 이전 기준이며, sync 가 변수 모드를 읽게 되면 자동으로 갱신된다. 수기로 고치지 않는다.

# Sidebar

- **노드 ID:** `69:5382` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Favorite, Default
- **States**: Default, Extended, Hover

## Variant 전체 (4)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Varient=Favorite, States=Default | W×H 256×1080, padding(TRBL) -/12/-/12 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7) | Title/Title5-SemiBold, Body/Body1-SemiBold | shadow/sm |
| Varient=Default, States=Extended | W×H 256×1080, padding(TRBL) -/12/-/12 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7) | Title/Title5-SemiBold, Body/Body1-SemiBold | shadow/sm |
| Varient=Default, States=Hover | W×H 256×1080, padding(TRBL) -/12/-/12 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Blue-100 (#E3EDFF), Blue-700 (#003EFF) | Title/Title5-SemiBold, Body/Body1-SemiBold | shadow/sm |
| Varient=Default, States=Default | W×H 256×1080, padding(TRBL) -/12/-/12 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7) | Title/Title5-SemiBold, Body/Body1-SemiBold | shadow/sm |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · gap 24

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Varient=Favorite, States=Default` — 배경 **Grey-50 (#FFFFFF)** · 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · gap 24
- Frame 1000007000 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · 크기 232×107]
  - Frame 1000007777 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 94×25]
    - Attention (instance) [가로 고정/세로 고정 · 크기 18×25] · → Sort=Attention, Color=Black
    - (시스템명) (text) [가로 hug/세로 hug · 크기 60×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-900 (#000000)
  - Search (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×38] · 배경 Grey-50 (#FFFFFF), 선 Grey-200 (#EAEDF0)
    - Icon / Search (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Search
    - PlaceholderText (text) [가로 fill/세로 hug · grow 1.0 · 크기 180×20] · 텍스트 Body/Body1-SemiBold · 색 Grey-400 (#A4AAB0)
- Frame 1000007001 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · 크기 232×312]
  - Tab (frame) [레이아웃 세로(V) · 가로 hug/세로 hug · 크기 232×40]
    - Menu (frame) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 232×40] · 배경 Grey-100 (#F5F6F7)
  - List (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · 크기 232×256]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×34] · 배경 Grey-50 (#FFFFFF)
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×34] · 배경 Grey-50 (#FFFFFF)
    - Sidebar / SidebarMenuItem (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · 크기 232×72]
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×34] · 배경 Grey-50 (#FFFFFF)
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×34] · 배경 Grey-50 (#FFFFFF)
    - Sidebar / SidebarMenuButton (frame) [레이아웃 가로(H) · 가로 fill/세로 고정 · 크기 232×34] · 배경 Grey-50 (#FFFFFF)

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Default / Favorite) 변화 시 → 달라짐: **없음(동일 형태, 조합만 다름)** · 동일: 크기, 배경, 보더, 자식 색, 레이아웃, 텍스트, 이펙트
- **States** (Default / Extended / Hover) 변화 시 → 달라짐: **자식 색** · 동일: 크기, 배경, 보더, 레이아웃, 텍스트, 이펙트

## 사용 규칙

- **크기·간격:** 폭 256, 좌우 padding 12, 항목 간 gap 24. **메뉴 항목(SidebarMenuButton) 높이 34**, **검색창 높이 38**.
- **로고:** 상단 브랜드 심볼은 **Attention 로고 SVG(18×25)** + 우측 **시스템명 텍스트(`Title5`, `Grey-900`) 필수**. 로고를 Lucide 등 아이콘으로 대체 금지, 시스템명 생략 금지.
- **텍스트:** 메뉴 항목 `Body1`, 검색 placeholder `Body1`(`Grey-400`).
- **활성/hover:** 활성 메뉴만 `Blue-700` 전경 + `Blue-100` 배경. 배경은 흰색.
- **금지:** 메뉴 항목 높이 40, 검색창 36, 시스템명 누락, placeholder를 `Body2`로 쓰는 것.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).