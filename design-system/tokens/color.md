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
| 슬로우베드 | `slowbed` | `#0D207C` | `#D7E4F0` |
| 레터스 | `letus` | `#FF5C39` | `#FFF3ED` |
| 퍼플식스 | `purplesix` | `#7800F5` | `#F4E8FF` |
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
