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

## 상태 태그 매핑

상태 5범주 매핑(대기 black-light / 보류 yellow-light / 진행중 green-light / 완료 blue-light / 취소·실패 요약카드 red-dark·테이블 red-light)과 **라벨 텍스트는 업무 용어 그대로**(결제완료→완료 금지 등), 6번째 색 금지 규칙은 **`CLAUDE.md` 「상태 태그 5범주 매핑」이 정본**이다. 여기서 값을 중복 정의하지 않는다.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

