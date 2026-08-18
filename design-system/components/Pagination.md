# Pagination

- **노드 ID:** `69:9226` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Pagination | W×H 176×20 | **투명** | — | Grey-900 (#000000), Grey-400 (#A4AAB0) | Body/Body1-SemiBold, Body/Body2-Regular | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 12

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Pagination` — 배경 **투명** · 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 12
- Icon / ChevronLeft (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / ChevronLeft
  - Vector (vector) [크기 4×8] · 선 Grey-900 (#000000)
- 숫자 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 120×20]
  - 1 (text) [가로 hug/세로 hug · 크기 6×20] · 텍스트 Body/Body1-SemiBold · 색 Grey-900 (#000000)
  - 2 (text) [가로 hug/세로 hug · 크기 8×20] · 텍스트 Body/Body2-Regular · 색 Grey-400 (#A4AAB0)
  - 3 (text) [가로 hug/세로 hug · 크기 9×20] · 텍스트 Body/Body2-Regular · 색 Grey-400 (#A4AAB0)
  - 4 (text) [가로 hug/세로 hug · 크기 9×20] · 텍스트 Body/Body2-Regular · 색 Grey-400 (#A4AAB0)
  - 5 (text) [가로 hug/세로 hug · 크기 8×20] · 텍스트 Body/Body2-Regular · 색 Grey-400 (#A4AAB0)
- Icon / ChevronRight (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / ChevronRight
  - Vector (vector) [크기 4×8] · 선 Grey-900 (#000000)

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

