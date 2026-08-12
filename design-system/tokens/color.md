# Color — SIDIZ 컬러 토큰

원본: Figma `시디즈_디자인 시스템` (`UsCx1wPybDpRRBglYY5Nmx`), `2. Foundation` 페이지 파싱.
색상은 대부분 **Figma 변수(variables)** 로 정의돼 있어 값은 노드에서 확정되나, 시맨틱 별칭의 변수 *이름*은 REST로 안 나온다(변수 API는 Enterprise 전용).

## Primary (브랜드)

*용도:* Blue-700이 브랜드 포인트. 선택/링크/강조에만 절제 사용. Red는 에러 전용.

| 토큰 | 값 | 용도·규칙 |
|---|---|---|
| `Blue-700` | #003EFF | 브랜드 포인트(CTA 강조/선택/링크). 남용 금지 |
| `Blue-500` | #357FFF | 보조/hover 상태 |
| `Blue-100` | #E3EDFF | 선택·활성 **배경**(연한 파랑) |
| `Red-600` | #FF3A4A | 에러·경고 텍스트/보더 |
| `Red-100` | #FFECEE | 에러 배경(연한) |

## Grey (무채색 램프)

*용도:* 텍스트·보더·배경 기반. 50=흰색 배경, 900=검정. 임의 회색 발명 금지.

| 토큰 | 값 |
|---|---|
| `Grey-50` | #FFFFFF |
| `Grey-100` | #F5F6F7 |
| `Grey-200` | #EAEDF0 |
| `Grey-300` | #D6DADE |
| `Grey-400` | #A4AAB0 |
| `Grey-500` | #7C8084 |
| `Grey-600` | #595C5E |
| `Grey-700` | #434548 |
| `Grey-800` | #242526 |
| `Grey-900` | #000000 |

## Semantic (published FILL 스타일)

*파일에 스타일로 남아있는 시맨틱 별칭 6종. 값은 확정, 일부는 미사용.*

| 스타일 이름 | 값 | 비고 |
|---|---|---|
| `Semantic/Label/Strong` | #000000 | 강조 텍스트(=Grey-900) |
| `Semantic/Line/Normal/_Strong` | #70737C@0.52 | 진한 구분선(반투명) |
| `Semantic/Label/Normal` | #171719 | 기본 본문 텍스트 |
| `Main colors/Main Gray/main-gray_50` | #FEFEFE | ⚠️ Grey-50(#FFFFFF)와 다른 별도 gray |
| `Main colors/Main Gray/main-gray_500` | #9099B2 | ⚠️ Grey-500(#7C8084)와 다른 별도 gray |
| `Semantic/Primary/Normal` | [확인 필요] | [확인 필요] 파일 내 미적용→값 미확정 |

## 확인 필요

- 시맨틱 컬러(Label/Line/Background 등) 전체 체계는 **변수**로 존재 → 값은 컴포넌트에서 확인되나 변수 토큰명은 REST 미제공.
- `Semantic/Primary/Normal` 스타일 값(미적용).
- `Main Gray` 계열이 `Grey` 팔레트와 값이 달라(예: main-gray_50 #FEFEFE ≠ Grey-50 #FFFFFF) — 레거시/중복 여부 확인 필요.
