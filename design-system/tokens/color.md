# Color — SIDIZ 컬러 토큰

원본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), `sources/figma-raw.json` 파싱.
이 파일의 컬러는 **published FILL 스타일 63개**이며 대부분 **Light/Dark 모드 페어**를 가진다.

- 값 표기: `#RRGGBB`, 반투명은 `@불투명도`(예: `#70737C@0.16`).
- Light/Dark는 변수 모드 메타데이터가 REST로 제공되지 않아, **사용 컨텍스트 배경 명도로 유도**했다(대부분 명확, 3건은 `[L/D 확인필요]`).
- ⚠️ 이 토큰 체계는 구 `color.md`(gray/000~800, `text_*`, `#003EFF`)와 **다른 파일**이다. 신규 기준은 이 문서다.

## Primary (브랜드 액션)

*용도:* 주요 액션·강조. 버튼/링크/선택 등 브랜드 포인트. 남용 금지, 화면당 절제 사용.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Primary/Heavy` | #0054D1 | #0066FF |
| `Semantic/Primary/Normal` | #0066FF `[L/D 확인필요]` | #0066FF |
| `Semantic/Primary/Strong` | #005EEB | #1A75FF |

## Label (텍스트)

*용도:* 텍스트 색. Normal=본문, Strong=강조, Neutral/Alternative/Assistive=위계 낮춤, Disable=비활성.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Label/Alternative` | #37383C@0.61 | #AEB0B6@0.61 |
| `Semantic/Label/Assistive` | #37383C@0.28 | #AEB0B6@0.28 |
| `Semantic/Label/Disable` | #37383C@0.16 | #989BA2@0.16 |
| `Semantic/Label/Neutral` | #2E2F33@0.88 | #C2C4C8@0.88 |
| `Semantic/Label/Normal` | #171719 | #F7F7F8 |
| `Semantic/Label/Strong` | #000000 `[L/D 확인필요]` | #000000 |

## Background (배경)

*용도:* 면 배경. Normal=기본, Elevated=떠있는 면(카드/시트), Transparent=반투명 오버레이.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Background/Elevated/Alternative` | #F7F7F8 | #141415 |
| `Semantic/Background/Elevated/Normal` | #FFFFFF | #212225 |
| `Semantic/Background/Normal/Alternative` | #F7F7F8 | #0F0F10 |
| `Semantic/Background/Normal/Normal` | #FFFFFF | #1B1C1E |
| `Semantic/Background/Transparent/Alternative` | #FFFFFF@0.28 | #212225@0.61 |
| `Semantic/Background/Transparent/Normal` | #FFFFFF@0.08 | #212225@0.61 |

## Fill (보조 면)

*용도:* 버튼·칩 등 보조 면 채움. Strong>Normal>Alternative 순으로 옅어짐. 반투명 회색.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Fill/Alternative` | #70737C@0.05 | #70737C@0.12 |
| `Semantic/Fill/Normal` | #70737C@0.08 | #70737C@0.22 |
| `Semantic/Fill/Strong` | #70737C@0.16 | #70737C@0.28 |

## Line (보더/구분선)

*용도:* 테두리·구분선. Solid=불투명, Normal=반투명. _Strong>Normal>Neutral>Alternative 순.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Line/Normal/Alternative` | #70737C@0.08 | #70737C@0.22 |
| `Semantic/Line/Normal/Neutral` | #70737C@0.16 | #70737C@0.28 |
| `Semantic/Line/Normal/Normal` | #70737C@0.22 | #70737C@0.32 |
| `Semantic/Line/Normal/_Strong` | #70737C@0.52 | (단일) |
| `Semantic/Line/Solid/Alternative` | #F4F4F5 | #2E2F33 |
| `Semantic/Line/Solid/Neutral` | #EAEBEC | #333438 |
| `Semantic/Line/Solid/Normal` | #E1E2E4 | #37383C |

## Status (상태)

*용도:* 상태 표기. Positive=성공, Negative=에러, Cautionary=주의. 기능 표기로만 소량.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Status/Cautionary` | #FF9200 | #FFA938 |
| `Semantic/Status/Negative` | #FF4242 | #FF6363 |
| `Semantic/Status/Positive` | #00BF40 | #1ED45A |

## Interaction (상호작용)

*용도:* Disable=비활성 요소, Inactive=비활성 텍스트/아이콘.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Interaction/Disable` | #F4F4F5 | #2E2F33 |
| `Semantic/Interaction/Inactive` | #989BA2 | #5A5C63 |

## Inverse (반전)

*용도:* 반전 배경 위 요소(예: 툴팁/스낵바).

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Inverse/Background` | #1B1C1E | #FFFFFF |
| `Semantic/Inverse/Label` | #F7F7F8 | #171719 |
| `Semantic/Inverse/Primary` | #3385FF | #0066FF |

## Static (고정색)

*용도:* 모드와 무관하게 고정. 반전되면 안 되는 곳에만.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Static/Black` | #000000 | (단일) |
| `Semantic/Static/White` | #FFFFFF | (단일) |
| `Static/Black` | #000000 | (단일) |
| `Static/White` | #FFFFFF | (단일) |

## Material (오버레이)

*용도:* Dimmer=모달 뒤 딤 처리 오버레이.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Material/Dimmer` | #171719@0.52 | #171719@0.74 |

## Accent — Foreground (강조 전경)

*용도:* 데이터/강조용 전경(텍스트·아이콘) 색상 팔레트.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Accent/Foreground/Blue` | #005EEB | #4F95FF |
| `Semantic/Accent/Foreground/Cyan` | #0098B2 | #00BDDE |
| `Semantic/Accent/Foreground/Green` | #009632 | #1ED45A |
| `Semantic/Accent/Foreground/Light Blue` | #008DCF | #00AEFF |
| `Semantic/Accent/Foreground/Lime` | #429E00 | #58CF04 |
| `Semantic/Accent/Foreground/Orange` | #D17600 | #FF9200 |
| `Semantic/Accent/Foreground/Pink` | #E846CD | #FA73E3 |
| `Semantic/Accent/Foreground/Purple` | #AD36E3 | #D478FF |
| `Semantic/Accent/Foreground/Red` | #E52222 | #FF6363 |
| `Semantic/Accent/Foreground/Red Orange` | #F55A00 | #FF7B2E |
| `Semantic/Accent/Foreground/Violet` | #5B37ED | #9E86FC |

## Accent — Background (강조 배경)

*용도:* 데이터/강조용 배경 채움 색상 팔레트.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Semantic/Accent/Background/Cyan` | #00BDDE | #28D0ED |
| `Semantic/Accent/Background/Light Blue` | #00AEFF | #3DC2FF |
| `Semantic/Accent/Background/Lime` | #58CF04 | #6BE016 |
| `Semantic/Accent/Background/Pink` | #F553DA | #FA73E3 |
| `Semantic/Accent/Background/Purple` | #CB59FF | #D478FF |
| `Semantic/Accent/Background/Red Orange` | #FF5E00 | #FF7B2E |
| `Semantic/Accent/Background/Violet` | #6541F2 `[L/D 확인필요]` | #6541F2 |

## _Status (내부/주석)

*용도:* [확인 필요] 디자인 파일 내부 주석용 추정(Design Only 등). 프로덕트 토큰 아닐 수 있음.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `_Status/Design Only` | #F0ECFE | (단일) |
| `_Status/Normal` | #EAF2FE | (단일) |

## Legacy (비-Semantic 중복)

*용도:* Semantic/ 접두사 없는 구버전 중복 스타일. 신규 작업은 Semantic/* 사용 권장.

| 토큰 이름 | Light | Dark |
|---|---|---|
| `Background/Normal/Normal` | #FFFFFF | (단일) |
| `Background/Transparent/Alternative` | #FFFFFF@0.28 | (단일) |
| `Background/Transparent/Normal` | #FFFFFF@0.08 | (단일) |
| `Label/Normal` | #171719 | (단일) |
| `Label/Strong` | #000000 | (단일) |

## 확인 필요

- `Semantic/Accent/Background/Violet`, `Semantic/Label/Strong`, `Semantic/Primary/Normal` — 두 값은 확인됐으나 Light/Dark 배정이 컨텍스트상 모호(`[L/D 확인필요]`). 값 자체는 각각 `#6541F2`/`#7D5EF7`, `#000000`/`#FFFFFF`, `#0066FF`/`#3385FF`.
- `_Status/*` 2건: 프로덕트 토큰인지 디자인 주석용인지 용도 미확정.
