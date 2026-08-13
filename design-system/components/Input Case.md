# Input Case

- **노드 ID:** `66:2132` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Field, Text

## Variant 전체 (2)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Varient=Text | W×H 124×44 | Body/Body2-Regular, Body/Body3-SemiBold | Grey-900 (#000000), Grey-500 (#7C8084) | — | — |
| Varient=Field | W×H 314×84 | Body/Body2-Regular, Body/Body3-SemiBold, Body/Body4-Regular | Grey-500 (#7C8084), Grey-400 (#A4AAB0), Red-600 (#FF3A4A), Grey-50 (#FFFFFF) | Grey-200 (#EAEDF0), #EF2E32 | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 6

## 하위 구조 (대표 variant, 2~3레벨)

`Varient=Text` — 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · sizing 주축 hug/교차 hug · gap 6
- 서브 타이틀 (text) [가로 hug/세로 hug] · 텍스트 Body/Body3-SemiBold
- 텍스트를 입력해 주세요. (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Field / Text) 변화 시 → 달라짐: **fill, stroke, 크기, 텍스트** · 동일: 레이아웃, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

