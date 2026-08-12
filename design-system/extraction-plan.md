# Extraction Plan — Figma → design-system 문서 검수

원본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), 로컬 덤프 `sources/figma-raw.json` (REST, 5.4MB, 2026-08-12 재수신).
※ 파일이 전면 개편됨: 실제 SIDIZ UI 컴포넌트 + Foundation 팔레트 구성.

**상태:** ✅ 완료 · 🔄 진행중 · ⬜ 미착수 · ⚠️ 확인 필요

---

## [0] 자산 전수 검증 — ✅ 완료

- **스타일 62개**: TEXT 54 · FILL 6 · EFFECT 2. (색/간격/radius는 대부분 **변수**로 이전 → 값은 노드에서 확정, 변수명은 REST 미제공)
- **컴포넌트**: 트리 COMPONENT 100(독립 4 + 배리언트 96), COMPONENT_SET 15. map extra 52 중 45 remote(외부 로고).
- 페이지별:

| 페이지 | id | 노드 | COMPONENT | COMPONENT_SET |
|---|---|---|---|---|
| Cover | 0:1 | 15 | 0 | 0 |
| Updates | 4:399 | 52 | 0 | 0 |
| --- | 4:130 | 0 | 0 | 0 |
| 1. Logo | 4:476 | 62 | 4 | 2 |
| 2. Foundation | 5:1224 | 305 | 0 | 0 |
| 3. Component | 66:732 | 1725 | 96 | 13 |

## [1] tokens/color.md — ✅ 완료
Foundation 팔레트 15색(Blue/Red/Grey, 브랜드 **Blue-700 #003EFF**) + 시맨틱 FILL 6.

## [2] tokens/typography.md — ✅ 완료
TEXT 53종(중복 제거) — 주 스케일 Title/Body/Caption, ko/*, en/*, 컴팩트 UI, 레거시로 그룹핑.

## [3] tokens/spacing.md — ✅ 완료
변수 바인딩 값 집계로 radius/padding/gap 스케일 정리(토큰명은 [확인 필요]).

## [4] tokens/effect.md — ✅ 완료
EFFECT 2종(Drop Shadow 2겹, shadow/sm).

## [5] components/ — 🔄 진행중 (19단위)

목록 순서대로 하나씩 `components/[이름].md` 작성 → 체크 → 커밋.

### 로고 (1. Logo)
- ✅ Attention — set `66:4004`
- ✅ Signature — set `66:3929`

### UI 컴포넌트 (3. Component)
- ✅ Button — set `69:6191`
- ⬜ Input — set `69:7170`
- ⬜ Input Case — set `66:2132`
- ⬜ Checkbox — set `66:1863`
- ⬜ Radio — set `66:1837`
- ⬜ Dropdown List — set `66:2543`
- ⬜ Search Filter — set `66:1886`
- ⬜ Tab — set `66:2256`
- ⬜ Tag — set `69:6068`
- ⬜ Table Cell — set `66:1794`
- ⬜ Toast Popup — set `66:1681`
- ⬜ Carousel — set `69:9181`
- ⬜ Sidebar — set `69:5382`
- ⬜ Breadcrumb — component `69:8870`
- ⬜ Dashboard Card — component `69:8975`
- ⬜ Header — component `68:4651`
- ⬜ Pagination — component `69:9226`

---

## 진행 로그
- 2026-08-11: 구 파일 기반 초안 → 신 파일(구버전) 토큰 재작성.
- 2026-08-12: 파일 전면 개편 재수신. [0]~[4] 재작성 완료(팔레트 #003EFF 복귀 등). [5] 컴포넌트 19단위 착수.
