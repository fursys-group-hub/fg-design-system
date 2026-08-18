# Search Filter

- **노드 ID:** `66:1886` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Default, Extended

## Variant 전체 (2)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| State=Extended | W×H 1280×241, padding(TRBL) 16/-/16/-, radius 4 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-500 (#7C8084), Red-600 (#FF3A4A), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-900 (#000000) | Caption/Caption1-SemiBold, Body/Body2-Regular, Body/Body3-SemiBold, Body/Body1-SemiBold | — |
| State=Default | W×H 1280×91, padding(TRBL) 16/-/16/-, radius 4 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-500 (#7C8084), Red-600 (#FF3A4A), Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-400 (#A4AAB0), Grey-900 (#000000) | Caption/Caption1-SemiBold, Body/Body2-Regular, Body/Body3-SemiBold, Body/Body1-SemiBold | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 세로(V) · 주축 정렬 끝 · 교차 정렬 끝 · gap 8

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`State=Extended` — 배경 **Grey-50 (#FFFFFF)** · 방향 세로(V) · 주축 정렬 끝 · 교차 정렬 끝 · gap 8
- Frame 1000007021 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · 크기 1280×209]
  - Frame 1000007760 (frame) [레이아웃 세로(V) · 가로 fill/세로 hug · grow 1.0 · 크기 1070×209]
    - Frame 1000007765 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · 크기 1070×59]
    - Frame 1000007766 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · 크기 1070×59]
    - Frame 1000007767 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · 크기 1070×59]
  - Frame 1000007015 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 162×32]
    - Button (frame) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 87×32]
    - Button (instance) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 71×32] · 배경 Grey-50 (#FFFFFF), 선 Grey-200 (#EAEDF0), → Varient=Secondary, Shape=Round
- Frame 1000007062 (frame) [레이아웃 가로(H) · 가로 고정/세로 고정 · 크기 24×24] · 배경 Grey-50 (#FFFFFF), 선 Grey-200 (#EAEDF0)
  - Icon / ChevronUp (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / ChevronUp
    - Vector (vector) [크기 8×4] · 선 Grey-900 (#000000)

## Variant 차이 (무엇이 바뀌나)

- **State** (Default / Extended) 변화 시 → 달라짐: **크기** · 동일: 배경, 보더, 자식 색, 레이아웃, 텍스트, 이펙트

## 사용 규칙

- **일정(기간) 필드:** 날짜 범위(`0000/00/00 - 0000/00/00`)는 **한 줄 유지 — 줄바꿈 금지(`white-space: nowrap`)**. 좁으면 **폭을 늘려서라도** 1줄로 둔다.
- 기간 필드 폭: **Input Case min-width 348px**(내부 날짜 Input 208px, Calendar 아이콘 16). layoutWrap=NO_WRAP.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

