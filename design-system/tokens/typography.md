# Typography — SIDIZ 타이포그래피 토큰

정본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`, 2026-08-12 재수신) → **`2. Foundation` Typography**.
**Pretendard 단일 · line-height 150% · letter-spacing 1%** 공통. 14종 체계.
주 토큰명 = 실제 Figma 스타일명, `별칭`·용도 병기.

## Title

| 토큰 (Figma 스타일) | 별칭 | Size | Weight | LH | LS | 용도 |
|---|---|---|---|---|---|---|
| `Title/Title1-SemiBold` | Title1 | 40px | SemiBold (600) | 150% | 1% | 프로모션 대제목 |
| `Title/Title2-SemiBold` | Title2 | 26px | SemiBold (600) | 150% | 1% | 프로모션 중제목 |
| `Title/Title3-SemiBold` | Title3 | 22px | SemiBold (600) | 150% | 1% | 페이지 메인 타이틀 |
| `Title/Title4-SemiBold` | Title4 | 16px | SemiBold (600) | 150% | 1% | 섹션 타이틀 |
| `Title/Title5-SemiBold` | Title5 | 14px | SemiBold (600) | 150% | 1% | Card/Modal 타이틀 |

## Body

| 토큰 (Figma 스타일) | 별칭 | Size | Weight | LH | LS | 용도 |
|---|---|---|---|---|---|---|
| `Body/Body1-SemiBold` | Body1 | 13px | SemiBold (600) | 150% | 1% | 그룹 타이틀 |
| `Body/Body2-Regular` | Body2 | 13px | Regular (400) | 150% | 1% | 그룹 타이틀 보조 |
| `Body/Body3-SemiBold` | Body3 | 12px | SemiBold (600) | 150% | 1% | 본문 강조 |
| `Body/Body4-Regular` | Body4 | 12px | Regular (400) | 150% | 1% | 기본 본문 |

## Caption

| 토큰 (Figma 스타일) | 별칭 | Size | Weight | LH | LS | 용도 |
|---|---|---|---|---|---|---|
| `Caption/Caption1-SemiBold` | Caption1 | 11px | SemiBold (600) | 150% | 1% | Label, 헬프 텍스트 |
| `Caption/Caption2-SemiBold` | Caption2 | 10px | SemiBold (600) | 150% | 1% | 뱃지, 태그 텍스트 |
| `Caption/Caption3-Regular` | Caption3 | 10px | Regular (400) | 150% | 1% | 서브 문구 |
| `Caption/Caption4-SemiBold` | Caption4 | 8px | SemiBold (600) | 150% | 1% | 최소 표기 강조 |
| `Caption/Caption5-Regular` | Caption5 | 8px | Regular (400) | 150% | 1% | 최소 표기 |

## 확정 체계 대조

사용자 확정 체계와 Figma 적용 스타일 **14종 전부 일치** (Pretendard / LH 150% / LS 1%, size·weight 동일). 불일치 없음.
LH 150% 실측 px = size×1.5 (40→60, 13→19.5, 8→12 …) 정확히 일치. LS 1% 실측 px = size×0.01.

## Foundation 안내표와 다른 항목

- Foundation `2. Foundation` 페이지에 **구 세대 스타일 프레임이 아직 잔존**: `ko/*`(Pretendard), `en/*`(Centra No2), 레거시 `Pretendard JP`(Title 2·3/Bold, Body 1/Normal-*), px 명시 컴팩트(`Body/Body4-12-Regular`, `Caption/Caption2-10-Semibold` 등). **이들은 정본 아님** → 이 문서에서 제외.
- `Body 1/Normal - Bold` — 파일 내 미적용, 값 추출 불가.
