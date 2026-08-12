# Button

- **노드 ID:** `69:6191` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Primary, Secondary, Disabled, Error
- **Shape**: Square, Round, Text, Flat

## Variant 전체 (12)

| variant | 크기·간격 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Error, Shape=Square | W×H 78×28, padding(TRBL) -/12/-/12, radius 4, gap 6 | Body/Body3-SemiBold | Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Red-600 (#FF3A4A) | — |
| Varient=Disabled, Shape=Flat | W×H 63×20, padding(TRBL) -/8/-/8, radius 9999, gap 6 | Caption/Caption1-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Flat | W×H 63×20, padding(TRBL) 2/8/2/8, radius 9999, gap 6 | Caption/Caption1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Flat | W×H 63×20, padding(TRBL) -/8/-/8, radius 9999, gap 6 | Caption/Caption1-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |
| Varient=Secondary, Shape=Text | W×H 71×28, padding(TRBL) -/12/-/12, radius 9999, gap 6 | Caption/Caption1-SemiBold | Grey-400 (#A4AAB0) | Grey-400 (#A4AAB0) | — |
| Varient=Primary, Shape=Text | W×H 71×28, padding(TRBL) -/12/-/12, radius 9999, gap 6 | Caption/Caption1-SemiBold | Grey-900 (#000000) | Grey-900 (#000000) | — |
| Varient=Disabled, Shape=Round | W×H 78×28, padding(TRBL) -/12/-/12, radius 9999, gap 6 | Body/Body3-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Round | W×H 78×28, padding(TRBL) -/12/-/12, radius 9999, gap 6 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Round | W×H 78×28, padding(TRBL) -/12/-/12, radius 9999, gap 6 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |
| Varient=Disabled, Shape=Square | W×H 78×28, padding(TRBL) -/12/-/12, radius 4, gap 6 | Body/Body3-SemiBold | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Grey-400 (#A4AAB0) | — |
| Varient=Secondary, Shape=Square | W×H 78×28, padding(TRBL) -/12/-/12, radius 4, gap 6 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Primary, Shape=Square | W×H 78×28, padding(TRBL) -/12/-/12, radius 4, gap 6 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-50 (#FFFFFF) | — |

## 하위 구조 (대표 variant)

`Varient=Error, Shape=Square` → Icon / Search(instance), 버튼명(text)

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

