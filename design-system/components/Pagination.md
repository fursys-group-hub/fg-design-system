# Pagination

- **노드 ID:** `69:9226` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Pagination | W×H 176×20 | Body/Body1-SemiBold, Body/Body2-Regular | Grey-900 (#000000), Grey-400 (#A4AAB0) | Grey-900 (#000000) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 hug/교차 hug · gap 12

## 하위 구조 (대표 variant, 2~3레벨)

`Pagination` — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · sizing 주축 hug/교차 hug · gap 12
- Icon / ChevronLeft (instance) [가로 고정/세로 고정] · → Icon / ChevronLeft
  - Vector (vector)
- 숫자 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug]
  - 1 (text) [가로 hug/세로 hug] · 텍스트 Body/Body1-SemiBold
  - 2 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular
  - 3 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular
  - 4 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular
  - 5 (text) [가로 hug/세로 hug] · 텍스트 Body/Body2-Regular
- Icon / ChevronRight (instance) [가로 고정/세로 고정] · → Icon / ChevronRight
  - Vector (vector)

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

