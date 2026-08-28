# Color — SIDIZ 컬러 토큰

정본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`) → **`2. Foundation` 페이지 Color 프레임**.
Foundation에 없는 published 스타일(`Semantic/*`, `Main colors/Main Gray/*`)은 구 세대 잔존물이므로 이 문서에서 제외한다.

## Primary Colors (브랜드별 · 2톤)

*용도:* Primary-600 이 브랜드 포인트(버튼 배경·사이드바 활성·라인탭 밑줄·섹션 건수). Primary-200 은 사이드바 활성 배경.
**9개 브랜드마다 값이 다르며 600/200 두 톤만** 쓴다. `<html data-brand="...">` 로 전환(기본: 그룹사 공통).

| 토큰 | CSS 변수 | 용도·규칙 |
|---|---|---|
| `Primary-600` | `--fg-color-primary-600` | 브랜드 포인트. 강조/선택/링크/건수에만 절제 사용 |
| `Primary-200` | `--fg-color-primary-200` | 브랜드 강조 **배경**(사이드바 활성 배경) |

### 브랜드별 Primary 값 (9)

| 브랜드 | data-brand | Primary-600 | Primary-200 |
|---|---|---|---|
| 시디즈 | `sidiz` | `#003EFF` | `#E3EDFF` |
| 퍼시스 | `fursys` | `#E3001C` | `#FCE5E8` |
| 일룸 | `iloom` | `#D60707` | `#FEDADA` |
| 데스커 | `desker` | `#272727` | `#E9E9E9` |
| 알로소 | `alloso` | `#B14E3F` | `#F7EDEC` |
| 슬로우베드 | `sloubed` | `#0D207C` | `#D7E4F0` |
| 레터스 | `letus` | `#FF5C39` | `#FFF3ED` |
| 퍼플식스 | `p6` | `#7800F5` | `#F4E8FF` |
| 그룹사 공통(기본) | `group` | `#6725F3` | `#F0E9FE` |

## System Colors (9브랜드 공통 · 각 600/100)

*용도:* 상태 색. 600=전경/채움, 100=연한 배경. 완료=Blue, 진행중=Green, 보류=Yellow, 취소/실패·에러=Red.

| 토큰 | 값 | 용도·규칙 |
|---|---|---|
| `Red-600` | `#EF2E32` | 취소/실패·에러 텍스트/보더/채움 |
| `Red-100` | `#FBE7E7` | 취소/실패·에러 **배경**(연한) |
| `Yellow-600` | `#D4A300` | 보류 전경/채움 |
| `Yellow-100` | `#F9F1D9` | 보류 **배경**(연한) |
| `Green-600` | `#2AA75E` | 진행중 전경/채움 |
| `Green-100` | `#DFF2E7` | 진행중 **배경**(연한) |
| `Blue-600` | `#3769DE` | 완료 전경/채움 |
| `Blue-100` | `#EBF0FC` | 완료 **배경**(연한) |
| `Gray-600` | `#909090` | System 무채 전경(Grey Scale 와 별개) |
| `Gray-100` | `#F0F0F0` | System 무채 배경 |

## Grey Scale

*용도:* 텍스트·보더·배경 기반 무채색 10단계. 50=흰색, 900=검정. 임의 회색 발명 금지.

| 토큰 | 값 |
|---|---|
| `Grey-900` | `#000000` |
| `Grey-800` | `#242526` |
| `Grey-700` | `#434548` |
| `Grey-600` | `#595C5E` |
| `Grey-500` | `#7C8084` |
| `Grey-400` | `#A4AAB0` |
| `Grey-300` | `#D6DADE` |
| `Grey-200` | `#EAEDF0` |
| `Grey-100` | `#F5F6F7` |
| `Grey-50` | `#FFFFFF` |

## Secondary Colors (고객 화면 전용 · 브랜드별)

*용도:* 고객 화면(랜딩·브랜드·프로모션)의 **섹션 배경·보조 강조 전용.** **업무 시스템 화면에서 쓰지 않는다.** 변수는 `--fg-secondary-{계열}-{번호}`(계열 소문자, 두 단어는 하이픈: `purple-gray`·`silver-sand`). 정본 값은 `dist/fg/tokens.css` 의 `[data-brand]` 블록.

- **숫자는 Grey Scale 의 밝기 위치**를 뜻한다. `Primary-500` 과 `Secondary-500` 은 같은 밝기다.
- 예외: **일룸의 Yellow·Blue 는 10단계 램프**로 브랜드 가이드의 원래 번호를 그대로 쓴다(밝기 기준이 아니다).
- 브랜드마다 **개수와 계열이 다르며, 없는 브랜드도 있다.**

### 시디즈 (sidiz) — 1개

| 계열 | 번호 | HEX |
|---|---|---|
| blue | 500 | `#357FFF` |

### 퍼시스 (fursys) — 11개

| 계열 | 번호 | HEX |
|---|---|---|
| orange | 400 | `#F47018` |
| yellow | 400 | `#FFAF05` |
| olive | 500 | `#828705` |
| green | 500 | `#309F2E` |
| cornflower | 500 | `#6B8FE5` |
| lilac | 400 | `#C6AEE0` |
| brown | 700 | `#4F360D` |
| slate | 500 | `#37847D` |
| mint | 300 | `#A5D3CE` |
| sky | 400 | `#67C0FF` |
| blue | 500 | `#0075EA` |

### 일룸 (iloom) — 20개

| 계열 | 번호 | HEX |
|---|---|---|
| yellow | 900 | `#A77300` |
| yellow | 800 | `#CC9514` |
| yellow | 700 | `#E5AF33` |
| yellow | 600 | `#F6C351` |
| yellow | 500 | `#FFD176` |
| yellow | 400 | `#FFD86D` |
| yellow | 300 | `#FFE087` |
| yellow | 200 | `#FFEAA7` |
| yellow | 100 | `#FFF3CC` |
| yellow | 50 | `#FFFAEA` |
| blue | 900 | `#184AA6` |
| blue | 800 | `#1857C2` |
| blue | 700 | `#1A64DA` |
| blue | 600 | `#2172EB` |
| blue | 500 | `#3182F6` |
| blue | 400 | `#4593FC` |
| blue | 300 | `#64A8FF` |
| blue | 200 | `#90C2FF` |
| blue | 100 | `#C9E2FF` |
| blue | 50 | `#E8F3FF` |

### 데스커 (desker) — 5개

| 계열 | 번호 | HEX |
|---|---|---|
| blue | 600 | `#285FE5` |
| yellow | 300 | `#FFDC1D` |
| red | 500 | `#F72A35` |
| green | 400 | `#00B441` |
| coral | 500 | `#FF5948` |

### 알로소 (alloso) — 19개

| 계열 | 번호 | HEX |
|---|---|---|
| wine | 800 | `#492829` |
| wine | 700 | `#714042` |
| wine | 300 | `#DAD0CE` |
| purple-gray | 600 | `#616273` |
| purple-gray | 400 | `#9A9AA6` |
| purple-gray | 300 | `#CECDD0` |
| butter | 500 | `#907A62` |
| butter | 400 | `#D0BE9B` |
| butter | 300 | `#EBDFCF` |
| forest | 700 | `#304442` |
| forest | 600 | `#4F5B5A` |
| forest | 300 | `#CDD4CF` |
| cozy | 600 | `#786156` |
| cozy | 400 | `#B9AB9C` |
| cozy | 300 | `#DFD9CD` |
| silver-sand | 500 | `#8A9397` |
| silver-sand | 400 | `#B4B9BC` |
| silver-sand | 300 | `#DBDEE0` |
| silver-sand | 200 | `#EDEFF2` |

### 슬로우베드 (sloubed) — 1개

| 계열 | 번호 | HEX |
|---|---|---|
| brown | 500 | `#9A7859` |

### 레터스 (letus) — 2개

| 계열 | 번호 | HEX |
|---|---|---|
| navy | 800 | `#003054` |
| navy | 200 | `#DBE4F2` |

### 퍼플식스 (p6) — 2개

| 계열 | 번호 | HEX |
|---|---|---|
| green | 300 | `#23F364` |
| green | 100 | `#F3FFDA` |

### 그룹사 공통 (group) — 4개

| 계열 | 번호 | HEX |
|---|---|---|
| green | 500 | `#008051` |
| green | 400 | `#01C979` |
| green | 300 | `#48E8A8` |
| orange | 500 | `#FF480E` |

> 합계 **65개** (sidiz 1·fursys 11·iloom 20·desker 5·alloso 19·sloubed 1·letus 2·p6 2·group 4).

## 컴포넌트 로컬 색 — 폐지 (System 으로 편입)

기존 로컬 확장색(Tag Green/Yellow·Toast Alert)은 **System 색으로 편입되어 더 이상 로컬 색이 아니다.** 컴포넌트에서 아래 System 변수로 참조한다.

| 옛 로컬 색 | 대체 System 토큰 |
|---|---|
| Tag Green 전경 `#38BA77` / 배경 `#E7F6E7` | `Green-600` `#2AA75E` / `Green-100` `#DFF2E7` |
| Tag Yellow 전경 `#E8C32E` / 배경 `#FCF7DF` | `Yellow-600` `#D4A300` / `Yellow-100` `#F9F1D9` |
| Toast Alert `#F5CA1D` | `Yellow-600` `#D4A300` |

> ⚠️ 2026-08 색 구조 개편: Primary(브랜드별 2톤) + System 10 + Grey Scale 10 = **22색**. 기존 단일 브랜드 Blue(`Blue-700/500/100`)는 폐지되고 Primary(브랜드별)로 대체됐다. 이 변경은 Figma **변수 모드** 기반이라 `/sync`(REST)로 읽지 못해 **수기 반영**했다(추후 변수 모드 동기화 가능해지면 sync 로 재생성).

## 로고 자산 색 (Logo asset — UI 색 아님)

*로고 아트워크에만 쓰는 색. **팔레트도 allowlist도 아니며, UI(텍스트·배경·보더)에 사용 금지.***

| 값 | 사용 범위 (한정) | 비고 |
|---|---|---|
| `#1D1D1B` | **Signature 로고 벡터**(`66:3931`~`66:3935`)와 그 인스턴스 | 브랜드 로고 근검정. 이 노드 밖에서 fill로 쓰면 위반 |

> Sidebar 등에서 보이는 `#1D1D1B`는 모두 Signature 로고 인스턴스(`I…;66:3931`)이며, 컴포넌트 고유 색이 아니다.

## 가이드/문서 색 (Figma 정리용 — 검사 제외)

*디자인 색이 아니라 Figma 편집·문서 정리용 색. 정본 토큰 아님. design-qa는 위치 무관 **검사 제외**하고 제외 건수만 집계한다.*

- `#8A38F5` — 컴포넌트 세트/인스턴스 표시 테두리
- `#9747FF` — 이미지 플레이스홀더 기본색
- `#F9F4FF` — 로고 전시/정리용 배경(로고 배경 아님)
