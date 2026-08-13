# Search Filter

- **노드 ID:** `66:1886` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Default, Extended

## Variant 전체 (2)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| State=Extended | W×H 1280×241, padding(TRBL) 16/-/16/-, radius 4 | Body/Body1-SemiBold, Body/Body2-Regular, Body/Body3-SemiBold, Caption/Caption1-SemiBold | Grey-900 (#000000), Grey-500 (#7C8084), Grey-400 (#A4AAB0), Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | — |
| State=Default | W×H 1280×91, padding(TRBL) 16/-/16/-, radius 4 | Body/Body1-SemiBold, Body/Body2-Regular, Body/Body3-SemiBold, Caption/Caption1-SemiBold | Grey-900 (#000000), Grey-500 (#7C8084), Grey-400 (#A4AAB0), Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 세로(V) · 주축 정렬 끝 · 교차 정렬 끝 · sizing 주축 hug/교차 고정 · gap 8

## 하위 구조 (대표 variant, 2~3레벨)

`State=Extended` — 방향 세로(V) · 주축 정렬 끝 · 교차 정렬 끝 · sizing 주축 hug/교차 고정 · gap 8
- Frame 1000007021 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
  - Frame 1000007760 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · grow 1.0]
    - Frame 1000007765 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
    - Frame 1000007766 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
    - Frame 1000007767 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
  - Frame 1000007015 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
    - Button (frame) [레이아웃 가로(H) · 가로 hug/세로 고정]
    - Button (instance) [레이아웃 가로(H) · 가로 hug/세로 고정] · → Varient=Secondary, Shape=Round
- Frame 1000007062 (frame) [레이아웃 가로(H) · 가로 고정/세로 고정]
  - Icon / ChevronUp (instance) [가로 고정/세로 고정] · → Icon / ChevronUp
    - Vector (vector)

## Variant 차이 (무엇이 바뀌나)

- **State** (Default / Extended) 변화 시 → 달라짐: **크기** · 동일: 레이아웃, 텍스트, fill, stroke, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

