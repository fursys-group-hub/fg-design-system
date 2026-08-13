# Toast Popup

- **노드 ID:** `66:1681` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Default, Error, Alert

## Variant 전체 (3)

| variant | 크기·간격 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| State=Alert | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6, gap 100 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), #F5CA1D, Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |
| State=Error | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6, gap 100 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |
| State=Default | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6, gap 100 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Blue-500 (#357FFF), Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |

## 하위 구조 (대표 variant)

`State=Alert` → Frame 1000007709(frame), Button(instance)

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

