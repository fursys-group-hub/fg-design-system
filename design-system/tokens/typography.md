# Typography — SIDIZ 타이포그래피 토큰

원본: Figma `시디즈_디자인 시스템` (node `1-184`).
스타일 **이름과 굵기(weight) 체계는 확인됨**. **font-size · line-height · letter-spacing 수치는 미확보(`[확인 필요]`)** — 이번 세션에 Figma MCP 호출 한도로 못 읽음. 한도 해제 후 채운다.

---

## 1. 폰트 패밀리 ✅ (매핑) / 수치 [확인 필요]

| 토큰 | 값 | 용도 | 사용 규칙 |
|---|---|---|---|
| 국문 폰트 | Pretendard | 한글 텍스트 | 모든 국문에 사용. |
| 영문/숫자 폰트 | Centra No.2 | 영문·숫자 | 영문·숫자에 사용. 미설치 환경 폴백은 `[확인 필요]`(스킬 문서상 Pretendard 폴백). |
| letter-spacing | `[확인 필요]` | 자간 | 본문 자간. (스킬 문서상 `-0.02em(-2%)`로 알려져 있으나 Figma 재확인 필요) |

Figma에는 `weight` · `letter-spacing` 축이 별도로 정의돼 있음. 웹 폰트 다운로드 링크 노드 존재(경로 `[확인 필요]`).

---

## 2. 타입 스케일

각 스타일의 **weight 조합은 확인됨**(Centra / Pretendard 순). **크기·행간은 `[확인 필요]`.**
표기: `Centra weight / Pretendard weight`.

### Title

| 토큰 이름 | size / line-height | weight (Centra / Pretendard) | 용도 | 사용 규칙 |
|---|---|---|---|---|
| `title1` | `[확인 필요]` | thin(280) / thin(100) | 최상위 제목 | 가장 큰 헤드라인. |
| `title2` | `[확인 필요]` | Light(300)·thin(280) / Light(300)·thin(100) | 대제목 | |
| `title3` | `[확인 필요]` | Light(300) / Light(300) | 제목 | |
| `title4` | `[확인 필요]` | book(400)·Light(300) / Light(300) | 제목 | |
| `title5` | `[확인 필요]` | `[확인 필요]` | 제목 | 수치·weight 모두 미확인. |
| `title6` | `[확인 필요]` | `[확인 필요]` | 제목 | 수치·weight 모두 미확인. |
| `title7` | `[확인 필요]` | medium(500)·book(400) / medium(500)·Regular(400) | 소제목 | |

### Body

| 토큰 이름 | size / line-height | weight (Centra / Pretendard) | 용도 | 사용 규칙 |
|---|---|---|---|---|
| `Body1` | `[확인 필요]` | medium(500)·book(400)·Light(300) / medium(500)·regular(400)·Light(300) | 서브타이틀·본문 겸용 | |
| `Body2` | `[확인 필요]` | medium(500)·book(400) / medium(500)·regular(400) | 본문 | |
| `Body3` | `[확인 필요]` | `[확인 필요]` | 본문 | 수치·weight 모두 미확인. |
| `Body4` | `[확인 필요]` | book(400) / regular(400) | 본문(소) | |

### Caption

| 토큰 이름 | size / line-height | weight | 용도 | 사용 규칙 |
|---|---|---|---|---|
| `Caption1` | `[확인 필요]` | `[확인 필요]` | 캡션 | |
| `Caption2` | `[확인 필요]` | `[확인 필요]` | 최소 텍스트 크기 | **본문 최소 크기.** 이보다 작은 텍스트 금지. 실제 px 값 `[확인 필요]`. |

---

## 확인 필요 목록 (요약)

- [ ] Centra No.2 미설치 폴백 폰트
- [ ] letter-spacing 실제 값
- [ ] 모든 스타일의 font-size / line-height
- [ ] `title5`, `title6`, `Body3`, `Caption1`, `Caption2`의 weight
- [ ] 웹 폰트 다운로드 링크 경로
