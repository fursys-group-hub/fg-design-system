# Typography — SIDIZ 타이포그래피 토큰

원본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), `sources/figma-raw.json` 파싱.
published TEXT 스타일 37개(중복 제거). 국문 `ko/*`(Pretendard) · 영문 `en/*`(Centra No2) 2트랙.

- 값 단위: fontSize·lineHeight·letterSpacing 모두 **px**. 괄호는 자간의 상대값(size 대비).
- 국문 본문 자간은 대체로 **-2%**로 일관(구 문서의 '-2%'와 일치, 이제 실측 확정).
- weight 체계도 구 문서와 일치(예: 타이틀1 Pretendard 100 / title1 Centra 280).

## 국문 ko/* (Pretendard)

| 스타일 이름 | fontFamily | weight | size | lineHeight | letterSpacing |
|---|---|---|---|---|---|
| `ko/바디1_l` | Pretendard | 300 | 18 | 25.2 | -0.36 (-2.0%) |
| `ko/바디2` | Pretendard | 400 | 15 | 24 | -0.3 (-2.0%) |
| `ko/바디3` | Pretendard | 400 | 14 | 22.4 | -0.28 (-2.0%) |
| `ko/바디4` | Pretendard | 400 | 13 | 15.6 | -0.26 (-2.0%) |
| `ko/캡션1` | Pretendard | 400 | 12 | 14.3 | -0.24 (-2.0%) |
| `ko/캡션2` | Pretendard | 400 | 11 | 13.1 | -0.22 (-2.0%) |
| `ko/타이틀1` | Pretendard | 100 | 88 | 105.6 | -1.76 (-2.0%) |
| `ko/타이틀2_l` | Pretendard | 300 | 54 | 64.8 | -1.08 (-2.0%) |
| `ko/타이틀3_t` | Pretendard | 100 | 40 | 56 | -0.8 (-2.0%) |
| `ko/타이틀4_l` | Pretendard | 300 | 34 | 47.6 | -0.68 (-2.0%) |
| `ko/타이틀5_l` | Pretendard | 300 | 30 | 42 | -0.6 (-2.0%) |
| `ko/타이틀6_l` | Pretendard | 300 | 26 | 36.4 | -0.52 (-2.0%) |
| `ko/타이틀7` | Pretendard | 400 | 22 | 30.8 | -0.44 (-2.0%) |

## 영문·숫자 en/* (Centra No2)

| 스타일 이름 | fontFamily | weight | size | lineHeight | letterSpacing |
|---|---|---|---|---|---|
| `en/body2_m` | Centra No2 | 500 | 15 | 24 | -0.3 (-2.0%) |
| `en/body3` | Centra No2 | 400 | 14 | 22.4 | -0.28 (-2.0%) |
| `en/body4` | Centra No2 | 400 | 13 | 15.6 | -0.26 (-2.0%) |
| `en/caption1` | Centra No2 | 400 | 12 | 15.6 | -0.24 (-2.0%) |
| `en/caption2` | Centra No2 | 400 | 11 | 14.3 | -0.22 (-2.0%) |
| `en/title1` | Centra No2 | 280 | 88 | 105.6 | -1.76 (-2.0%) |
| `en/title2_l` | Centra No2 | 300 | 54 | 64.8 | -1.08 (-2.0%) |
| `en/title3_t` | Centra No2 | 280 | 40 | 56 | -0.8 (-2.0%) |
| `en/title4_l` | Centra No2 | 300 | 34 | 47.6 | -0.68 (-2.0%) |
| `en/title5_l` | Centra No2 | 300 | 30 | 42 | -0.6 (-2.0%) |
| `en/title6_l` | Centra No2 | 300 | 26 | 36.4 | -0.52 (-2.0%) |
| `en/title7` | Centra No2 | 400 | 22 | 30.8 | -0.44 (-2.0%) |

## 레거시/외부 임포트 (Pretendard JP 등)

*아래는 `ko/` `en/` 체계 밖의 스타일. 외부 라이브러리에서 임포트된 것으로 보이며, 신규 작업은 `ko/`·`en/` 사용 권장.*

| 스타일 이름 | fontFamily | weight | size | lineHeight | letterSpacing |
|---|---|---|---|---|---|
| `Body 1/Normal - Medium` | Pretendard JP | 500 | 16 | 24 | 0.091 (0.6%) |
| `Body/Body2-Regular` | Pretendard | 400 | 16 | 25.6 | -0.16 (-1.0%) |
| `Body/Body3-SemiBold` | Pretendard | 600 | 14 | 22.4 | -0.14 (-1.0%) |
| `Caption 1/Bold` | Pretendard JP | 600 | 12 | 16 | 0.302 (2.5%) |
| `Caption 2/Bold` | Pretendard JP | 600 | 11 | 14 | 0.342 (3.1%) |
| `Display 3/Bold` | Pretendard JP | 700 | 36 | 48 | -0.972 (-2.7%) |
| `Heading 2/Bold` | Pretendard JP | 600 | 20 | 28 | -0.24 (-1.2%) |
| `Headline 2/Bold` | Pretendard JP | 600 | 17 | 24 | 0 (0.0%) |
| `Title 2/Bold` | Pretendard JP | 700 | 28 | 38 | -0.661 (-2.4%) |
| `Title 3/Bold` | Pretendard JP | 700 | 24 | 32 | -0.552 (-2.3%) |

## 사용 규칙 (요약)

- 국문 화면은 `ko/*`, 영문·숫자 표기는 `en/*` 사용. 혼용 시 baseline 정렬 주의.
- 타이틀1~7 = 헤드라인 스케일(큰→작은), 바디1~4 = 본문, 캡션1~2 = 최소 텍스트.
- **캡션2(11px)가 최소 크기.** 이보다 작은 본문 금지.

## 확인 필요

- `Body 1/Normal - Bold` — 파일 내 어떤 노드에도 적용되지 않아 값 추출 불가(정의만 존재). size/weight `[확인 필요]`.
- 레거시 `Pretendard JP` 스타일들의 프로덕트 사용 여부(임포트 잔여물일 가능성).
