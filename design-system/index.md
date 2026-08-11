# SIDIZ 디자인 시스템 — 기준서 (index)

이 폴더(`design-system/`)는 SIDIZ 디자인의 **원본 기준서(source of truth)** 다.
모든 디자인 관련 작업 전에 이 문서를 먼저 읽는다.

- 값의 최종 원본은 Figma 파일 `시디즈_디자인 시스템`
  (`figma.com/design/UsCx1wPybDpRRBglYY5Nmx`)이며, 로컬 덤프는 `sources/figma-raw.json`(REST)이다.
- 이 폴더의 문서는 그 Figma 값을 마크다운으로 옮긴 기준서다. `tokens.css` 등 코드 파일은
  이 문서에서 변환해 생성하며, 지금은 만들지 않는다.

## 토큰 문서

| 문서 | 내용 | 상태 |
|---|---|---|
| [tokens/color.md](tokens/color.md) | Semantic 컬러(Label/Background/Line/Primary/Accent…) Light·Dark | ✅ FILL 63 반영 |
| [tokens/typography.md](tokens/typography.md) | ko/* · en/* 타입 스케일 | ✅ TEXT 37 반영 |
| [tokens/spacing.md](tokens/spacing.md) | 간격·radius | ✅ (정식 토큰 부재 확인) |
| [tokens/effect.md](tokens/effect.md) | 그림자(DROP_SHADOW) | ✅ EFFECT 7 반영 |
| [extraction-plan.md](extraction-plan.md) | 추출 체크리스트·진행 로그 | 🔄 [5] 컴포넌트 보류 |

## 작성 원칙

세부 원칙은 저장소 루트 `CLAUDE.md`의 "디자인 시스템 문서 작성 원칙"을 따른다. 요약:

- 토큰 형식: **토큰 이름 / 값 / 용도 / 사용 규칙**
- 못 읽었거나 불확실한 값은 **추측하지 말고 `[확인 필요]`** 로 남긴다.
- 문서 1개는 **500줄 이내**. 넘으면 분할한다.
