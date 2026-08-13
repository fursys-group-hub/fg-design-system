# Toast Popup

- **노드 ID:** `66:1681` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Default, Error, Alert

## Variant 전체 (3)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| State=Alert | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), #F5CA1D, Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |
| State=Error | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |
| State=Default | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Blue-500 (#357FFF), Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | #B3B3B3, Grey-50 (#FFFFFF) | Drop Shadow |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · sizing 주축 고정/교차 hug · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 100는 최소 간격)

## 하위 구조 (대표 variant, 2~3레벨)

`State=Alert` — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · sizing 주축 고정/교차 hug · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 100는 최소 간격)
- Frame 1000007709 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
  - Icon / CircleAlertFill (frame) [가로 고정/세로 고정]
    - Frame 4185 (frame)
  - 최초 로그인 시 비밀번호 재설정이 필요합니다. (text) [가로 hug/세로 hug] · 텍스트 Body/Body1-SemiBold
- Button (instance) [레이아웃 가로(H) · 가로 hug/세로 고정] · → Varient=Secondary, Shape=Text
  - Icon / Plus (instance) [가로 고정/세로 고정] · → Icon / Plus
    - Vector (vector)
  - 버튼명 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular

## Variant 차이 (무엇이 바뀌나)

- **State** (Alert / Default / Error) 변화 시 → 달라짐: **fill** · 동일: 크기, 레이아웃, 텍스트, stroke, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

