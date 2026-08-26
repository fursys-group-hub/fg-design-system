> ⚠️ 이 파일은 피그마 실측 기록이다. 색 이름은 2026-08-26 구조 개편 이전 기준이며, sync 가 변수 모드를 읽게 되면 자동으로 갱신된다. 수기로 고치지 않는다.

# Tab

- **노드 ID:** `66:2256` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **Varient**: Box, Line

## Variant 전체 (2)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| Varient=Line | W×H 570×40 | **투명** | Grey-200 (#EAEDF0) | Grey-50 (#FFFFFF), Blue-700 (#003EFF), Grey-800 (#242526), Grey-900 (#000000), Grey-400 (#A4AAB0), Grey-500 (#7C8084), Grey-300 (#D6DADE) | Title/Title5-SemiBold | shadow/sm |
| Varient=Box | W×H 608×40 | **투명** | — | Grey-100 (#F5F6F7), Grey-50 (#FFFFFF), Grey-800 (#242526), Grey-900 (#000000), Grey-500 (#7C8084), Grey-400 (#A4AAB0) | Title/Title5-SemiBold, Body/Body2-Regular | shadow/sm |

## 레이아웃 (오토레이아웃)

- **Varient=Line**: 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 시작 · gap 0
- **Varient=Box**: 방향 세로(V) · 주축 정렬 시작 · 교차 정렬 시작 · gap 0

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`Varient=Line` — 배경 **투명** · 방향 가로(H) · 주축 정렬 시작 · 교차 정렬 시작 · gap 0
- Select (frame) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 114×40] · 배경 투명(Transparent), 선 Blue-700 (#003EFF)
  - Icon / Sun (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Sun
    - Vector (vector) [크기 13×13] · 선 Grey-800 (#242526)
  - 선택 메뉴명 (text) [가로 hug/세로 hug · 크기 65×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-900 (#000000)
  - 100 (text) [가로 hug/세로 hug · 크기 25×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-400 (#A4AAB0)
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정 · 크기 114×40] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Sun
    - Vector (vector) [크기 13×13] · 선 Grey-500 (#7C8084)
  - Tabs Text (text) [가로 hug/세로 hug · 크기 37×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-300 (#D6DADE)
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정 · 크기 114×40] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Sun
    - Vector (vector) [크기 13×13] · 선 Grey-500 (#7C8084)
  - Tabs Text (text) [가로 hug/세로 hug · 크기 37×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-300 (#D6DADE)
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정 · 크기 114×40] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Sun
    - Vector (vector) [크기 13×13] · 선 Grey-500 (#7C8084)
  - Tabs Text (text) [가로 hug/세로 hug · 크기 37×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-300 (#D6DADE)
- Default (instance) [레이아웃 가로(H) · 가로 고정/세로 고정 · 크기 114×40] · → Active=Off
  - Icon / Sun (instance) [가로 고정/세로 고정 · 크기 16×16] · → Icon / Sun
    - Vector (vector) [크기 13×13] · 선 Grey-500 (#7C8084)
  - Tabs Text (text) [가로 hug/세로 hug · 크기 37×21] · 텍스트 Title/Title5-SemiBold · 색 Grey-300 (#D6DADE)

## Variant 차이 (무엇이 바뀌나)

- **Varient** (Box / Line) 변화 시 → 달라짐: **레이아웃, 보더, 자식 색, 크기, 텍스트** · 동일: 배경, 이펙트

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).