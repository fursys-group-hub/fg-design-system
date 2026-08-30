# Effect — SIDIZ 그림자 토큰

원본: Figma `퍼시스그룹_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`). EFFECT 스타일 2종.

| 토큰 | 레이어 | x | y | blur | spread | color | 용도 |
|---|---|---|---|---|---|---|---|
| `Drop Shadow` | 1 | 0 | 4 | 6 | -2 | #000000@0.05 | 팝오버/드롭다운/카드 부양 |
|  | 2 | 0 | 10 | 15 | -3 | #000000@0.10 |  |
| `shadow/sm` | 1 | 0 | 1 | 2 | 0 | #000000@0.05 | 미세 상승(입력/작은 요소) |

## 사용 규칙

- 기본은 border 구분, 그림자는 떠 있는 표면에만. `Drop Shadow`는 2겹 합성.

## 잔존 스타일 (정본 아님 — 2026-08-20 원본 실측)

Internal Only Canvas의 **외부 라이브러리 잔재**(Switch, DropdownMenu)에서만 사용되는 스타일. **정본 아님** — 신규 화면에서 사용 금지.

| 토큰 | 레이어 | x | y | blur | spread | color | 사용처(잔재) |
|---|---|---|---|---|---|---|---|
| `shadow/md` | 1 | 0 | 2 | 4 | -1 | #000000@0.06 | Switch, DropdownMenu (외부 라이브러리) |
|  | 2 | 0 | 4 | 6 | -1 | #000000@0.10 |  |
| `shadow/lg` | — | — | — | — | — | `Drop Shadow`와 동일 값 | Switch, DropdownMenu (외부 라이브러리) |
