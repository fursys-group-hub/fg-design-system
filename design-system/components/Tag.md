# Tag

- **노드 ID:** `69:6068` (COMPONENT_SET)
- **소속 페이지:** 3. Component

## Variant 속성

- **State**: Light, Dark
- **Color**: Red, Green, Blue, Gray, Yellow, Black

## Variant 전체 (12)

> **배경**=컨테이너 자체 fill, **보더**=컨테이너 자체 stroke. 자식 요소(텍스트·아이콘)의 색·크기는 아래 **하위 구조** 참조.

| variant | 크기 | 배경(컨테이너) | 보더 | 자식 색(텍스트·아이콘·포인트) | 텍스트 토큰 | 이펙트 |
|---|---|---|---|---|---|---|
| State=Dark, Color=Black | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Grey-900 (#000000)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Black | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Grey-50 (#FFFFFF)** | Grey-200 (#EAEDF0) | Grey-900 (#000000) | Caption/Caption1-SemiBold | — |
| State=Dark, Color=Gray | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Grey-400 (#A4AAB0)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Gray | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Grey-100 (#F5F6F7)** | — | Grey-400 (#A4AAB0) | Caption/Caption1-SemiBold | — |
| State=Dark, Color=Blue | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Blue-500 (#357FFF)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Blue | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Blue-100 (#E3EDFF)** | — | Blue-500 (#357FFF) | Caption/Caption1-SemiBold | — |
| State=Dark, Color=Green | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **#38BA77 (로컬 확장색)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Green | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **#E7F6E7 (로컬 확장색)** | — | #38BA77 (로컬 확장색) | Caption/Caption1-SemiBold | — |
| State=Dark, Color=Yellow | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **#E8C32E (로컬 확장색)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Yellow | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **#FCF7DF (로컬 확장색)** | — | #E8C32E (로컬 확장색) | Caption/Caption1-SemiBold | — |
| State=Dark, Color=Red | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Red-600 (#FF3A4A)** | — | Grey-50 (#FFFFFF) | Caption/Caption1-SemiBold | — |
| State=Light, Color=Red | W×H 28×16, padding(TRBL) -/4/-/4, radius 2 | **Red-100 (#FFECEE)** | — | Red-600 (#FF3A4A) | Caption/Caption1-SemiBold | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 0

## 하위 구조 (대표 variant, 2~3레벨 · 요소별 색·크기)

`State=Dark, Color=Black` — 배경 **Grey-900 (#000000)** · 방향 가로(H) · 주축 정렬 가운데 · 교차 정렬 가운데 · gap 0
- 태그 (text) [가로 hug/세로 hug · 크기 20×17] · 텍스트 Caption/Caption1-SemiBold · 색 Grey-50 (#FFFFFF)

## Variant 차이 (무엇이 바뀌나)

- **State** (Dark / Light) 변화 시 → 달라짐: **배경, 보더, 자식 색** · 동일: 크기, 레이아웃, 텍스트, 이펙트
- **Color** (Black / Blue / Gray / Green / Red / Yellow) 변화 시 → 달라짐: **배경, 보더, 자식 색** · 동일: 크기, 레이아웃, 텍스트, 이펙트

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

