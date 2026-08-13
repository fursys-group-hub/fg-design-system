# Dropdown List

- **노드 ID:** `66:2543` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Single, Multiple, Profile
- **State**: Default, Hover

## Variant 전체 (5)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Profile, State=Default | W×H 195×243, radius 4 | Body/Body2-Regular, Body/Body3-SemiBold, Caption/Caption1-SemiBold, Title/Title5-SemiBold | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | Drop Shadow |
| Varient=Multiple, State=Hover | W×H 220×256, radius 4 | Body/Body2-Regular, Body/Body4-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Multiple, State=Default | W×H 220×260, radius 4 | Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | Grey-400 (#A4AAB0), Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Single, State=Hover | W×H 220×260, radius 4 | Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | — |
| Varient=Single, State=Default | W×H 220×260, radius 4 | Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | Grey-400 (#A4AAB0), Grey-200 (#EAEDF0) | — |

## 레이아웃 (오토레이아웃)

- **Varient=Profile, State=Default**: 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 0
- **Varient=Multiple, State=Hover 외 3종**: 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 고정 · gap 0

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Profile, State=Default` — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 0
- Profile (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
  - Frame 3916 (frame) [레이아웃 세로(V) · 가로 hug/세로 hug]
    - Frame 1000007758 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
    - email_adress@fursys.com (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular
- Settings (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
  - Language (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
    - Section (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · stretch]
    - Select (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
- Log Out (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · stretch]
  - Icon / LogOut (instance) [가로 고정/세로 고정] · → Icon / LogOut
    - Vector (vector)
  - 로그아웃 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Multiple / Profile / Single) 변화 시 → 달라짐: **fill, stroke, 레이아웃, 이펙트, 크기, 텍스트** · 동일: —
- **State** (Default / Hover) 변화 시 → 달라짐: **fill, stroke, 크기, 텍스트** · 동일: 레이아웃, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

