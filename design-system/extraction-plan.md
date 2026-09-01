# Extraction Plan — Figma → design-system 문서 검수

원본: Figma `퍼시스그룹_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), 로컬 덤프 `sources/figma-raw.json` (REST, 5.4MB, 2026-08-12 재수신).
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

## [5] components/ — ✅ 완료 (19단위)

목록 순서대로 하나씩 `components/[이름].md` 작성 → 체크 → 커밋.

### 로고 (1. Logo)
- ✅ Attention — set `66:4004`
- ✅ Signature — set `66:3929`

### UI 컴포넌트 (3. Component)
- ✅ Button — set `69:6191`
- ✅ Input — set `69:7170`
- ✅ Input Case — set `66:2132`
- ✅ Checkbox — set `66:1863`
- ✅ Radio — set `66:1837`
- ✅ Dropdown List — set `66:2543`
- ✅ Search Filter — set `66:1886`
- ✅ Tab — set `66:2256`
- ✅ Tag — set `69:6068`
- ✅ Table Cell — set `66:1794`
- ✅ Toast Popup — set `66:1681`
- ✅ Carousel — set `69:9181`
- ✅ Sidebar — set `69:5382`
- ✅ Breadcrumb — component `69:8870`
- ✅ Dashboard Card — component `69:8975`
- ✅ Header — component `68:4651`
- ✅ Pagination — component `69:9226`

---

## 진행 로그
- 2026-08-11: 구 파일 기반 초안 → 신 파일(구버전) 토큰 재작성.
- 2026-08-12: 파일 전면 개편 재수신. [0]~[4] 재작성 완료(팔레트 #003EFF 복귀 등). [5] 컴포넌트 19단위 전부 문서화·커밋 완료.
- 2026-08-12(2차): 타이포 전면 개편 재수신. typography.md를 신 체계(Title1~5/Body1~4/Caption1~5, Pretendard·LH150%·LS1%)로 재작성 — 확정 체계와 14종 전부 일치. 컴포넌트 19단위 재파싱(구조·노드ID 동일, 적용 토큰만 갱신). color/spacing/effect 무변경. **legacy 토큰 잔존 5개(Table Cell·Search Filter·Sidebar·Header·Dropdown List) — Figma 재적용 누락**.
- 2026-08-12(3차): Figma legacy 정리 완료. 재수신 검증 결과 **19 컴포넌트 정의·문서 legacy 토큰 0건(clean)**. published 구 px-named 스타일 8→1(`Body/Body4-12-Regular`만 잔존, 데모 프레임에서만 사용·컴포넌트 미사용). FILL 6→5(`Main colors/Main Gray/main-gray_500` 삭제됨).
- 2026-08-13(sync): `3. Component` 전면 수정 반영(lastModified 08-13T02:43:40Z). **14 컴포넌트 값 변경** — 텍스트 토큰 상향(Body4→Body2, Caption2→Caption1, Body3→Body1, Body1→Title7 등), 크기·gap 소폭 증가, Button padding 8→10 신규. Tag 로컬색 변경(Green #10C266→#38BA77, Yellow #F5CA1D→#E8C32E; Toast Alert는 #F5CA1D 유지). spacing.md padding 10 추가. 타이포 정본 14 값 무변경(Body2/Body3 동일이름 legacy 중복본 재출현은 무시). legacy 검사 clean. **비의도 유입: 새 `Page 7`(PC-2.1 목업)·Pagination 중복(89:1156)·shadow/sm EFFECT 중복 — 정본 미반영, 디자이너 정리 권장.**
