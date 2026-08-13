# Radio

- **노드 ID:** `66:1837` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Activated, Inactive, Hover

## Variant 전체 (3)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| State=Hover | W×H 16×16 | — | Grey-50 (#FFFFFF) | Grey-900 (#000000) | — |
| State=Inactive | W×H 16×16 | — | Grey-50 (#FFFFFF) | Grey-300 (#D6DADE) | — |
| State=Activated | W×H 16×16 | — | Grey-900 (#000000), Grey-50 (#FFFFFF) | Grey-900 (#000000) | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 오토레이아웃 없음 — 자식은 절대좌표(자유배치)

## 하위 구조 (대표 variant, 2~3레벨)

`State=Hover` — 오토레이아웃 없음 — 자식은 절대좌표(자유배치)
- Radio (frame)

## Variant 차이 (무엇이 바뀌나)

- **State** (Activated / Hover / Inactive) 변화 시 → 달라짐: **fill, stroke** · 동일: 크기, 레이아웃, 텍스트, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

