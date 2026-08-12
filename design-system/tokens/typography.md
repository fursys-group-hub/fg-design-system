# Typography — SIDIZ 타이포그래피 토큰

정본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`) → **`2. Foundation` 페이지 Typography 프레임**.
**Pretendard 단일**. 타이틀1~7 / 바디1~4 / 캡션1~2 만 정본으로 남긴다.
Foundation 밖의 스타일(`en/*` Centra No2, 컴팩트 UI px 스케일, 레거시 Pretendard JP)은 구 세대 잔존물이므로 제외한다.

값은 Foundation의 **스펙 표기**(Line-Height %/Auto, Letter-spacing %) 기준. 실측 px과 다른 항목은 하단 "스펙-실측 불일치" 참고.
(각 행의 Figma 스타일 = `Title/*`·`Body/*`·`Caption/*` 및 병행 `ko/*`)

## Title

| 토큰 | Size | Weight | Line-Height(스펙) | Letter-spacing(스펙) |
|---|---|---|---|---|
| `타이틀1` | 88px | Thin (100) | 120% | -2% |
| `타이틀2` | 54px | Light (300) | 120% | -2% |
| `타이틀3` | 40px | Thin (100) | 140% | -2% |
| `타이틀4` | 34px | Light (300) | 140% | -2% |
| `타이틀5` | 30px | Light (300) | 140% | -2% |
| `타이틀6` | 26px | Light (300) | 140% | -2% |
| `타이틀7` | 22px | Regular (400) | 140% | -2% |

## Body

| 토큰 | Size | Weight | Line-Height(스펙) | Letter-spacing(스펙) |
|---|---|---|---|---|
| `바디1` | 18px | Light (300) | 140% | -2% |
| `바디2` | 15px | Regular (400) | 140% | -2% |
| `바디3` | 14px | Regular (400) | 140% | -2% |
| `바디4` | 13px | Regular (400) | 140% | -2% |

## Caption

| 토큰 | Size | Weight | Line-Height(스펙) | Letter-spacing(스펙) |
|---|---|---|---|---|
| `캡션1` | 12px | Regular (400) | Auto | -2% |
| `캡션2` | 11px | Regular (400) | Auto | -2% |

## 사용 규칙

- 타이틀1~7 = 헤드라인(큰→작은), 바디1~4 = 본문, 캡션1~2 = 보조·최소 텍스트.
- **최소 크기 캡션2(11px)**. 이보다 작은 본문 금지.
- 자간 -2% 일관. 국문 Pretendard 단일.

## 스펙-실측 불일치

Foundation 스펙 표기와 실제 적용된 스타일의 px 값이 다른 항목. **표에는 Foundation 스펙을 정본으로 기재**했고, 실측은 아래에 기록한다.

| 토큰 | 스펙(Foundation) | 실측(적용 스타일) | 비고 |
|---|---|---|---|
| `바디2` | LH 140% (=21px) | **24px (≈160%)** | 실측이 스펙보다 큼 |
| `바디3` | LH 140% (=19.6px) | **22.4px (≈160%)** | 실측이 스펙보다 큼 |
| `바디4` | LH 140% (=18.2px) | **15.6px (≈120%)** | 실측이 스펙보다 작음 |
| `캡션1` | LH Auto | **고정 14.3px** | 스펙은 Auto인데 고정값 적용 |
| `캡션2` | LH Auto | **고정 13.1px** | 스펙은 Auto인데 고정값 적용 |

※ 타이틀1~7·바디1은 스펙과 실측 일치. 위 5건은 Figma 스타일 정의를 스펙에 맞춰 정정 필요.
