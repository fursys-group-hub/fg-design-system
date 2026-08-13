# Table Cell

- **노드 ID:** `66:1794` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Header, Cell
- **Type**: Checkbox, Text, Link, Textlink, Radio, Icon, Button, Tag, Calendar, Input

## Variant 전체 (13)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Header, Type=Text | W×H 52×32, padding(TRBL) -/16/-/16 | Caption/Caption1-SemiBold | #B3B3B3, Grey-100 (#F5F6F7) | Grey-200 (#EAEDF0), #ECECEC | — |
| Varient=Header, Type=Radio | W×H 48×32, padding(TRBL) -/16/-/16 | — | Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Header, Type=Checkbox | W×H 48×32, padding(TRBL) -/16/-/16 | — | Grey-100 (#F5F6F7), Grey-50 (#FFFFFF) | Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Calendar | W×H 128×38, padding(TRBL) -/16/-/16 | Body/Body2-Regular | Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Input | W×H 346×38, padding(TRBL) -/16/-/16 | Body/Body2-Regular | Grey-400 (#A4AAB0), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Icon | W×H 48×38, padding(TRBL) -/16/-/16 | — | Grey-50 (#FFFFFF) | Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Button | W×H 102×38, padding(TRBL) -/16/-/16 | Body/Body3-SemiBold | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000), Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Tag | W×H 60×38, padding(TRBL) -/16/-/16 | Caption/Caption1-SemiBold | Red-600 (#FF3A4A), Red-100 (#FFECEE), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Link | W×H 167×38, padding(TRBL) -/16/-/16 | Body/Body2-Regular | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Textlink | W×H 66×38, padding(TRBL) -/16/-/16 | Body/Body2-Regular | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Text | W×H 66×38, padding(TRBL) -/16/-/16 | Body/Body2-Regular | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Radio | W×H 48×38, padding(TRBL) -/16/-/16 | — | Grey-50 (#FFFFFF) | Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |
| Varient=Cell, Type=Checkbox | W×H 48×38, padding(TRBL) -/16/-/16 | — | Grey-50 (#FFFFFF) | Grey-300 (#D6DADE), Grey-200 (#EAEDF0) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 hug/교차 고정 · gap 0

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Header, Type=Text` — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 hug/교차 고정 · gap 0
- Frame 1000007707 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
  - 번호 (text) [가로 hug/세로 hug] · 텍스트 Caption/Caption1-SemiBold
- Line 1 (line) [가로 고정/세로 고정]

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Cell / Header) 변화 시 → 달라짐: **fill, stroke, 크기, 텍스트** · 동일: 레이아웃, 이펙트
- **Type** (Button / Calendar / Checkbox / Icon / Input / Link / Radio / Tag / Text / Textlink) 변화 시 → 달라짐: **fill, stroke, 크기, 텍스트** · 동일: 레이아웃, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

