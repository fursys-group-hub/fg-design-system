# Dashboard Card

- **노드 ID:** `69:8975` (COMPONENT)
- **소속 페이지:** 3. Component

## Variant 전체 (1)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Dashboard Card | W×H 314×65, padding(TRBL) 16/20/16/20, radius 4 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Grey-200 (#EAEDF0), Grey-900 (#000000) | Caption/Caption1-SemiBold, Title/Title3-SemiBold | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 0

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Dashboard Card` — 배경 **Grey-50 (#FFFFFF)** · 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 0
- Tag (instance) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 28×18] · 배경 Grey-50 (#FFFFFF), 선 Grey-200 (#EAEDF0), → State=Light, Color=Black
  - 태그 (text) [가로 hug/세로 hug · 크기 20×17] · 텍스트 Caption/Caption1-SemiBold · 색 Grey-900 (#000000)
- Frame 4192 (frame) [레이아웃 가로(H) · 가로 fill/세로 hug · grow 1.0 · 크기 246×33]
  - 100 (text) [가로 hug/세로 hug · 크기 39×33] · 텍스트 Title/Title3-SemiBold · 색 Grey-900 (#000000)
  - Frame 1000007756 (frame) [레이아웃 세로(V) · 가로 고정/세로 hug · 크기 11×22]
    - 건 (text) [가로 fill/세로 hug · 크기 11×17] · 텍스트 Caption/Caption1-SemiBold · 색 Grey-900 (#000000)

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

