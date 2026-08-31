# assets/ — 브랜드 로고 SVG (원본 보관용)

이 폴더의 SVG 는 **원본 보관용(source archive)** 이다. **화면에 실제로 렌더되는 로고는 `dist/fg/tokens.css` 의 `--fg-logo` / `--fg-logo-white`(base64 data URI)** 이며, 이 SVG 파일들은 그 base64 의 원본을 파일로 되살려 둔 것이다. 화면·컴포넌트에서 이 SVG 파일을 직접 참조하지 않는다(상대경로 링크는 저장소 밖 생성물에서 깨진다).

- 이 SVG 들은 `dist/fg/tokens.css` 의 base64 18개를 디코드해 만들었다(2026-08-31). 데스크톱 등에 별도 원본 벡터가 없어, tokens.css 의 base64 가 사실상 유일한 원본이었다.
- 값을 바꿔야 하면 **tokens.css 의 base64 와 이 SVG 를 함께** 갱신한다(둘이 어긋나지 않게).

## 파일 목록 (브랜드 코드 = data-brand)

| 브랜드 | 검정 | 흰색 | viewBox |
|---|---|---|---|
| 시디즈 | `sidiz.svg` | `sidiz-white.svg` | 60×85 |
| 퍼시스 | `fursys.svg` | `fursys-white.svg` | 80×80 |
| 일룸 | `iloom.svg` | `iloom-white.svg` | 240×67 |
| 데스커 | `desker.svg` | `desker-white.svg` | 380×60 |
| 알로소 | `alloso.svg` | `alloso-white.svg` | 300×69 |
| 슬로우베드 | `sloubed.svg` | `sloubed-white.svg` | 160×67 |
| 레터스 | `letus.svg` | `letus-white.svg` | 280×71 |
| 퍼플식스 | `p6.svg` | `p6-white.svg` | 300×147 |
| 그룹사 공통 | `group.svg` | — | 140×140 |

> **그룹사(group) 는 흰색 버전이 없다.** 어두운 배경에서도 **보라색(`#6726F3`) 로고를 그대로** 쓴다. 그래서 `group-white.svg` 는 만들지 않았고, `tokens.css` 의 `[data-brand="group"]` 도 `--fg-logo-white` 가 검정(보라)과 동일하다.

## Attention 심볼 (업무 시스템 공통)

- `attention-black.svg` / `attention-white.svg` — 업무 시스템 사이드바·헤더의 브랜드 심볼(Attention). 위 브랜드 로고와 별개다. Black=밝은 배경, White=어두운 배경.
