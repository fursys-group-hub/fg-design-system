# Table Cell

- **노드 ID:** `66:1794` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Header, Cell
- **Type**: Checkbox, Text, Link, Textlink, Radio, Icon, Button, Tag, Calendar, Input

## Variant 전체 (13)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Varient=Header, Type=Text | W×H 52×32, padding(TRBL) -/16/-/16 | **Grey-100 (#F5F6F7)** | Grey-200 (#EAEDF0) | #B3B3B3, #ECECEC | Caption/Caption1-SemiBold | — |
| Varient=Header, Type=Radio | W×H 48×32, padding(TRBL) -/16/-/16 | **Grey-100 (#F5F6F7)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-300 (#D6DADE) | — | — |
| Varient=Header, Type=Checkbox | W×H 48×32, padding(TRBL) -/16/-/16 | **Grey-100 (#F5F6F7)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-300 (#D6DADE) | — | — |
| Varient=Cell, Type=Calendar | W×H 128×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0) | Body/Body2-Regular | — |
| Varient=Cell, Type=Input | W×H 346×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0) | Body/Body2-Regular | — |
| Varient=Cell, Type=Icon | W×H 48×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-300 (#D6DADE) | — | — |
| Varient=Cell, Type=Button | W×H 102×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-900 (#000000) | Body/Body3-SemiBold | — |
| Varient=Cell, Type=Tag | W×H 60×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Red-100 (#FFECEE), Red-600 (#FF3A4A) | Caption/Caption1-SemiBold | — |
| Varient=Cell, Type=Link | W×H 167×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body2-Regular | — |
| Varient=Cell, Type=Textlink | W×H 66×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body2-Regular | — |
| Varient=Cell, Type=Text | W×H 66×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Body/Body2-Regular | — |
| Varient=Cell, Type=Radio | W×H 48×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-300 (#D6DADE) | — | — |
| Varient=Cell, Type=Checkbox | W×H 48×38, padding(TRBL) -/16/-/16 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-300 (#D6DADE) | — | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 0

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Varient=Header, Type=Text` — 배경 **Grey-100 (#F5F6F7)** · 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 0
- Frame 1000007707 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 20×17]
  - 번호 (text) [가로 hug/세로 hug · 크기 20×17] · 텍스트 Caption/Caption1-SemiBold · 색 #B3B3B3
- Line 1 (line) [가로 고정/세로 고정 · 크기 0×12] · 선 #ECECEC

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Cell / Header) 변화 시 → 달라짐: **배경, 자식 색, 크기, 텍스트** · 동일: 보더, 레이아웃, 이펙트
- **Type** (Button / Calendar / Checkbox / Icon / Input / Link / Radio / Tag / Text / Textlink) 변화 시 → 달라짐: **자식 색, 크기, 텍스트** · 동일: 배경, 보더, 레이아웃, 이펙트

## 사용 규칙

- **No.(번호) 컬럼:** 순번은 **순차 정수(1, 2, 3, 4, 5 …)** 로 표기한다. 주문번호·ID·역순 등 다른 형식으로 대체하지 않는다.
- Header 텍스트는 `Caption1`(11px), Cell 본문은 `Body2`(13px). 행 구분은 `Grey-200` hairline.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

