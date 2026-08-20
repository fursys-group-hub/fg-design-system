# Carousel

- **노드 ID:** `69:9181` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Indicator, Navigator

## Variant 전체 (2)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Varient=Indicator | W×H 168×6 | **투명** | — | Grey-50 (#FFFFFF), Grey-50 (#FFFFFF@0.30) | — | — |
| Varient=Navigator | W×H 80×30 | **투명** | — | Grey-50 (#FFFFFF@0.70), Grey-900 (#000000), Grey-800 (#242526) | — | — |

## 레이아웃 (오토레이아웃)

- **Varient=Indicator**: 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 12
- **Varient=Navigator**: 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 가운데 · gap 20

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Varient=Indicator` — 배경 **투명** · 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 12
- Ellipse 22 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF)
- Ellipse 23 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 24 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 25 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 26 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 27 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 28 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 29 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 30 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)
- Ellipse 31 (ellipse) [가로 고정/세로 고정 · 크기 6×6] · 배경 Grey-50 (#FFFFFF@0.30)

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Indicator / Navigator) 변화 시 → 달라짐: **레이아웃, 자식 색, 크기** · 동일: 배경, 보더, 텍스트, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

