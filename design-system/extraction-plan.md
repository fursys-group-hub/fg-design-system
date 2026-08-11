# Extraction Plan — Figma → design-system 문서 검수

원본(현행): Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), 로컬 덤프 `sources/figma-raw.json` (REST, 8.1MB).
※ 구 파일(`y2nbRqmwbrpMDmJdNvz15U` 시디즈닷컴 디자인에셋)과 **다른 파일·다른 토큰 체계**다.

**상태:** ✅ 완료 · 🔄 진행중 · ⬜ 미착수 · ⚠️ 확인 필요

---

## [0] 자산 전수 검증 — ✅ 완료

- 최상위 `components` 맵 111 vs 트리 78 → 차이 33 = **전부 `remote=True`**(원티드/퍼시스/시디즈 외부 로고). 로컬 78.
- 최상위 `componentSets` 맵 35 vs 트리 34 → 차이 1(`2:58`) = remote 로고 세트. 로컬 34.
- 페이지별:

| 페이지 | id | 총 노드 | COMPONENT | COMPONENT_SET |
|---|---|---|---|---|
| Cover | 0:1 | 15 | 0 | 0 |
| Updates | 4:399 | 52 | 0 | 0 |
| --- | 4:130 | 0 | 0 | 0 |
| **Foundation** | 4:131 | **0** | 0 | 0 | ← 원문 `children:[]`, 정말 비어있음 |
| Page 5 | 4:476 | 512 | 41 | 17 |
| Page 6 | 5:1224 | 9294 | 37 | 17 |

- **로컬 컴포넌트 38개 단위(셋 34 + 독립 4)는 전부 `Logo/Wanted*`** (원티드 로고). SIDIZ UI 컴포넌트 아님.

## [1] tokens/color.md — ✅ 완료
FILL 스타일 63개 → Light/Dark 페어로 정리. (12 단일 / 48 L·D 확정 / 3 L·D 확인필요)

## [2] tokens/typography.md — ✅ 완료
TEXT 스타일 37개(중복 제거) → ko/* 13, en/* 12, 레거시 10. size/lh/ls/weight 실측 채움.

## [3] tokens/spacing.md — ✅ 완료 (결론: 정식 토큰 없음)
spacing/grid/radius 스타일·변수 카테고리 부재. 관찰값만 기록, 나머지 `[확인 필요]`.

## [4] tokens/effect.md — ✅ 완료
EFFECT 스타일 7종(DROP_SHADOW) → x/y/blur/spread/color 정리.

## [5] components/ — ⚠️ 재확인 필요 (블로커)

**이 파일에 SIDIZ UI 컴포넌트(버튼/인풋/카드)가 없음.** 로컬 컴포넌트 38단위는 전부 원티드 로고:

- `Logo/Wanted/*`, `Logo/Wanted Gigs/*`, `Logo/Wanted Space/*`, `Logo/Wanted Sub Services/*`, `Logo/Wanted Partnership/*` (Page 5 / Page 6에 중복 존재)

→ 버튼/인풋/카드 문서화는 이 파일로 불가. 방향 결정 필요(아래 옵션은 최종 보고 참조).

---

## 진행 로그
- 2026-08-11: 구 파일 기반 초안 커밋(placeholder 다수).
- 2026-08-11: 신 파일 `UsCx1wPybDpRRBglYY5Nmx` REST 덤프. [0]~[4] 완료. 토큰 체계가 구 문서와 상이(Semantic 라이트/다크, `#0066FF` 등)하여 color/typography 전면 재작성. [5]는 UI 컴포넌트 부재로 보류.
