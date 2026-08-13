# Button

- **노드 ID:** `69:6191` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Primary, Secondary, Disabled, Error
- **Shape**: Square, Round, Text, Flat

## Variant 전체 (12)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Error, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | Body/Body1-SemiBold | Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Red-600 (#FF3A4A) | — |
| Varient=Disabled, Shape=Flat | W×H 70×24, padding(TRBL) -/10/-/10, radius 9999 | Body/Body3-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Flat | W×H 70×24, padding(TRBL) 2/10/2/10, radius 9999 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Flat | W×H 70×24, padding(TRBL) -/10/-/10, radius 9999 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |
| Varient=Secondary, Shape=Text | W×H 74×32, padding(TRBL) -/12/-/12, radius 9999 | Body/Body3-SemiBold | Grey-400 (#A4AAB0) | Grey-400 (#A4AAB0) | — |
| Varient=Primary, Shape=Text | W×H 74×32, padding(TRBL) -/12/-/12, radius 9999 | Body/Body3-SemiBold | Grey-900 (#000000) | Grey-900 (#000000) | — |
| Varient=Disabled, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | Body/Body1-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | Body/Body1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Round | W×H 82×32, padding(TRBL) -/12/-/12, radius 9999 | Body/Body1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |
| Varient=Disabled, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | Body/Body1-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | Body/Body1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Square | W×H 82×32, padding(TRBL) -/12/-/12, radius 4 | Body/Body1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · sizing 주축 hug/교차 고정 · gap 8

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Error, Shape=Square` — 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · sizing 주축 hug/교차 고정 · gap 8
- Icon / Search (instance) [가로 고정/세로 고정] · → Icon / Search
  - Vector (vector)
- 버튼명 (text) [가로 hug/세로 hug] · 텍스트 Body/Body1-SemiBold

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Disabled / Error / Primary / Secondary) 변화 시 → 달라짐: **fill, stroke, 크기** · 동일: 레이아웃, 텍스트, 이펙트
- **Shape** (Flat / Round / Square / Text) 변화 시 → 달라짐: **fill, stroke, 크기, 텍스트** · 동일: 레이아웃, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

