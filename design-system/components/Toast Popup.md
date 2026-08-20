# Toast Popup

- **노드 ID:** `66:1681` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Default, Error, Alert

## Variant 전체 (3)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| State=Alert | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | **Grey-900 (#000000)** | — | #F5CA1D (로컬 확장색), Grey-50 (#FFFFFF), Grey-400 (#A4AAB0), Grey-400 (#A4AAB0) | Body/Body1-SemiBold, Body/Body2-Regular | Drop Shadow |
| State=Error | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | **Grey-900 (#000000)** | — | Red-600 (#FF3A4A), Grey-50 (#FFFFFF), Grey-400 (#A4AAB0), Grey-400 (#A4AAB0) | Body/Body1-SemiBold, Body/Body2-Regular | Drop Shadow |
| State=Default | W×H 520×56, padding(TRBL) 12/32/12/32, radius 6 | **Grey-900 (#000000)** | — | Blue-500 (#357FFF), Grey-50 (#FFFFFF), Grey-400 (#A4AAB0), Grey-400 (#A4AAB0) | Body/Body1-SemiBold, Body/Body2-Regular | Drop Shadow |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 100는 최소 간격)

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`State=Alert` — 배경 **Grey-900 (#000000)** · 방향 가로(H) · 주축 정렬 양끝(SPACE_BETWEEN) · 교차 정렬 가운데 · 자식 **양끝 배치(SPACE_BETWEEN)** (itemSpacing 100는 최소 간격)
- Frame 1000007709 (frame) [레이아웃 가로(H) · 가로 hug/세로 hug · 크기 276×24]
  - Icon / CircleAlertFill (frame) [가로 고정/세로 고정 · 크기 24×24]
    - Frame 4185 (frame) [크기 24×24]
  - 최초 로그인 시 비밀번호 재설정이 필요합니다. (text) [가로 hug/세로 hug · 크기 236×20] · 텍스트 Body/Body1-SemiBold · 색 Grey-50 (#FFFFFF)
- Button (instance) [레이아웃 가로(H) · 가로 hug/세로 고정 · 크기 47×32] · → Varient=Secondary, Shape=Text
  - Icon / Plus (instance) [가로 고정/세로 고정 · 크기 12×12] · → Icon / Plus
    - Vector (vector) [크기 7×7] · 선 Grey-400 (#A4AAB0)
  - 버튼명 (text) [가로 hug/세로 hug · 크기 23×20] · 텍스트 Body/Body2-Regular · 색 Grey-400 (#A4AAB0)

## Variant 차이 (무엇이 바뀌나)

- **State** (Alert / Default / Error) 변화 시 → 달라짐: **자식 색** · 동일: 크기, 배경, 보더, 레이아웃, 텍스트, 이펙트

## 사용 규칙

- **배경은 다크(`Grey-900`/#000000), 텍스트는 흰색(`Grey-50`).** 밝은 배경 금지.
- **좌측:** 상태 아이콘 + 메시지(흰색 Body1). 상태 아이콘 색 = Default 파랑(`Blue-500`) / Error 빨강(`Red-600`) / Alert 노랑(`#F5CA1D`).
- **우측 액션:** **"닫기" 텍스트 버튼**(Secondary/Text, `Grey-400`)만 둔다. **X·Plus 등 아이콘을 넣지 않는다** — 정본 하위 구조에서 버튼 내 아이콘은 `HIDDEN`이고 라벨은 "닫기". 좌우 SPACE_BETWEEN.
- **크기·토큰:** 520×56, padding 12/32, radius 6, `Drop Shadow`. **상태 아이콘 24×24**, 메시지 `Body1`, **"닫기" 버튼 텍스트 `Body2`(13/400)**.
- **금지:** 상태 아이콘 20×20, "닫기" 텍스트를 `Body3`(12/600)로 쓰는 것, 밝은 배경.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

