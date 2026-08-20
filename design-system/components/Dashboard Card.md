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

## 사용 규칙

- **배열:** 요약 카드는 **가로(HORIZONTAL) 1행**으로 배열한다. **세로(상하) 스택 금지.** 카드 간 **gap 8px**, 4~5개를 1행으로.
- 카드 자체도 **내부 가로(HORIZONTAL) auto-layout**, **크기 314×65 고정**, padding 16/20, radius 4, 보더 `Grey-200`, **내부 gap 0**, 그림자 없음.
- **내부 구조(가로 1줄):** `Tag`(상태) + [수치 `Title3` + 단위 `Caption1`]. 수치·라벨을 **세로로 쌓지 않는다.** 수치 색은 상태 연동(에러=`Red-600`, 포인트=`Blue-700`, 기본=`Grey-900`).
- **금지:** 카드 내부 세로 스택·3줄 구성·`gap≠0`·높이 가변(65 초과). 이 경우 정본 위반이다.

## 상태 태그 매핑 (정본 규칙)

| 상태 범주 | 포함 예 | 태그 클래스 | 배경 | 글자 |
|---|---|---|---|---|
| 대기 | 접수, 승인 대기, 요청 대기 | `tag-black-light` | Grey-50 + Grey-200 보더 | Grey-900 |
| 보류 | 중지, 확인 필요 | `tag-yellow` | #FCF7DF | #E8C32E |
| 취소/실패 | 취소, 실패, 반려, 오류, 미매핑 | `tag-red-dark` | Red-600 | Grey-50 |
| 진행중 | 처리중, 배송중, 입고 진행, 조치중 | `tag-green` | #E7F6E7 | #38BA77 |
| 완료 | 승인, 입고 완료, 매핑 완료 | `tag-blue` | Blue-100 | Blue-500 |

- 새 상태값은 반드시 위 5범주 중 의미가 가장 가까운 곳에 매핑한다. **6번째 색을 만들지 않는다.**
- Light 태그의 글자색은 항상 같은 계열의 진한 색(전경색)을 쓴다.
- **Dashboard Card의 수치 색은 해당 상태 태그의 전경색을 그대로 따른다** (대기 Grey-900, 보류 #E8C32E, 취소/실패 Red-600, 진행중 #38BA77, 완료 Blue-500).

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

