# Button

- **노드 ID:** `69:6191` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Primary, Secondary, Disabled, Error
- **Shape**: Square, Round, Text, Flat

## Variant 전체 (12)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Varient=Error, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | **Grey-50 (#FFFFFF)** | Red-600 (#FF3A4A) | Red-600 (#FF3A4A) | Body/Body1-SemiBold | — |
| Varient=Disabled, Shape=Flat | W×H 70×24, padding(TRBL) -/10/-/10, radius 9999 | **Grey-200 (#EAEDF0)** | — | Grey-400 (#A4AAB0) | Body/Body3-SemiBold | — |
| Varient=Secondary, Shape=Flat | W×H 70×24, padding(TRBL) 2/10/2/10, radius 9999 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body3-SemiBold | — |
| Varient=Primary, Shape=Flat | W×H 70×24, padding(TRBL) -/10/-/10, radius 9999 | **Grey-900 (#000000)** | — | Grey-50 (#FFFFFF) | Body/Body3-SemiBold | — |
| Varient=Secondary, Shape=Text | W×H 74×32, padding(TRBL) -/12/-/12, radius 9999 | **투명** | — | Grey-400 (#A4AAB0) | Body/Body3-SemiBold | — |
| Varient=Primary, Shape=Text | W×H 74×32, padding(TRBL) -/12/-/12, radius 9999 | **투명** | — | Grey-900 (#000000) | Body/Body3-SemiBold | — |
| Varient=Disabled, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | **Grey-200 (#EAEDF0)** | — | Grey-400 (#A4AAB0) | Body/Body1-SemiBold | — |
| Varient=Secondary, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body1-SemiBold | — |
| Varient=Primary, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | **Grey-900 (#000000)** | — | Grey-50 (#FFFFFF) | Body/Body1-SemiBold | — |
| Varient=Disabled, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | **Grey-200 (#EAEDF0)** | — | Grey-400 (#A4AAB0) | Body/Body1-SemiBold | — |
| Varient=Secondary, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body1-SemiBold | — |
| Varient=Primary, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | **Grey-900 (#000000)** | — | Grey-50 (#FFFFFF) | Body/Body1-SemiBold | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 8

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Varient=Error, Shape=Square` — 배경 **Grey-50 (#FFFFFF)** · 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 8
- Icon / Search (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Search
  - Vector (vector) [크기 12×12] · 선 Red-600 (#FF3A4A)
- 버튼명 (text) [가로 hug/세로 hug · 크기 34×20] · 텍스트 Body/Body1-SemiBold · 색 Red-600 (#FF3A4A)

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Disabled / Error / Primary / Secondary) 변화 시 → 달라짐: **배경, 보더, 자식 색, 크기** · 동일: 레이아웃, 텍스트, 이펙트
- **Shape** (Flat / Round / Square / Text) 변화 시 → 달라짐: **배경, 보더, 자식 색, 크기, 텍스트** · 동일: 레이아웃, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

