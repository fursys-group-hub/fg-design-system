# Figma 정리 목록 — 정본 밖 색 교정 (생성 2026-08-20)

> 문서·`tokens.css`는 이미 정본 토큰으로 교정 완료. **Figma 원본에는 아직 아래 정본 밖 색이 남아 있어** 관리자가 직접 교정해야 한다.
> 교정 후 `/sync` 재덤프하면 문서가 정본으로 재생성된다. (생성기 `gen_component.py`는 정본 밖 색을 근사 토큰으로 자동 정규화하지만, **원본 자체를 정본 토큰 변수로 바인딩**하는 것이 목표다.)

파일: `시디즈_디자인 시스템` · 페이지 `3. Component` · lastModified 2026-08-13T07:54:52Z

## A. 교정 대상 (정본 토큰으로 치환)

| 컴포넌트 | variant | 레이어 | 속성 | 현재값 → 정본 토큰 | 노드 ID |
|---|---|---|---|---|---|
| Carousel | Varient=Navigator | Rectangle 3962 | stroke | #1A1A1A → **Grey-800** | `69:9196` |
| Carousel | Varient=Navigator | Rectangle 3962 | stroke | #1A1A1A → **Grey-800** | `69:9199` |
| Header | Header | Standard | fill | #FEFEFE → **Grey-50** | `I68:4636;298:20800` |
| Header | Header | Vector | fill | #FEFEFE → **Grey-50** | `I68:4636;2019:146403;2019:143205` |
| Input | Varient=Dropdown, State=Disabled | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7249;1:1101` |
| Input | Varient=Stepper, State=Default | Frame 2285 | stroke | #ECECEC → **Grey-200** | `69:7219` |
| Input | Varient=Stepper, State=Default | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7220;1:1111` |
| Input | Varient=Stepper, State=Default | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7222;1:1101` |
| Input | Varient=Stepper, State=Default | Vector 3 | stroke | #ECECEC → **Grey-200** | `69:7221` |
| Input | Varient=Stepper, State=Disabled | Frame 2285 | stroke | #ECECEC → **Grey-200** | `69:7198` |
| Input | Varient=Stepper, State=Disabled | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7199;1:1111` |
| Input | Varient=Stepper, State=Disabled | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7201;1:1101` |
| Input | Varient=Stepper, State=Disabled | Vector 3 | stroke | #ECECEC → **Grey-200** | `69:7200` |
| Input | Varient=Stepper, State=Filled | Frame 2285 | stroke | #ECECEC → **Grey-200** | `69:7205` |
| Input | Varient=Stepper, State=Filled | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7206;1:1111` |
| Input | Varient=Stepper, State=Filled | Vector | stroke | #B3B3B3 → **Grey-400** | `I69:7208;1:1101` |
| Input | Varient=Stepper, State=Filled | Vector 3 | stroke | #ECECEC → **Grey-200** | `69:7207` |
| Input Case | Varient=Field | Vector | stroke | #EF2E32 → **Red-600** | `I66:2142;1:1137` |
| Sidebar | Varient=Default, States=Default | Varient=Default, States=De | stroke | #ECECEC → **Grey-200** | `69:5464` |
| Sidebar | Varient=Default, States=Extended | Varient=Default, States=Ex | stroke | #ECECEC → **Grey-200** | `69:5419` |
| Sidebar | Varient=Default, States=Hover | Varient=Default, States=Ho | stroke | #ECECEC → **Grey-200** | `82:9521` |
| Sidebar | Varient=Favorite, States=Default | Varient=Favorite, States=D | stroke | #ECECEC → **Grey-200** | `69:5383` |
| Tab | Varient=Box | Vector | stroke | #18181B → **Grey-800** | `I66:2273;753:23394;1:3113` |
| Tab | Varient=Box | Vector | stroke | #71717A → **Grey-500** | `I66:2274;753:23450;1:3113` |
| Tab | Varient=Box | Vector | stroke | #71717A → **Grey-500** | `I66:2275;753:23450;1:3113` |
| Tab | Varient=Box | Vector | stroke | #71717A → **Grey-500** | `I66:2276;753:23450;1:3113` |
| Tab | Varient=Box | Vector | stroke | #71717A → **Grey-500** | `I66:2277;753:23450;1:3113` |
| Tab | Varient=Line | Vector | stroke | #18181B → **Grey-800** | `I66:2259;1:3113` |
| Tab | Varient=Line | Vector | stroke | #71717A → **Grey-500** | `I66:2262;753:23450;1:3113` |
| Tab | Varient=Line | Vector | stroke | #71717A → **Grey-500** | `I66:2263;753:23450;1:3113` |
| Tab | Varient=Line | Vector | stroke | #71717A → **Grey-500** | `I66:2264;753:23450;1:3113` |
| Tab | Varient=Line | Vector | stroke | #71717A → **Grey-500** | `I81:9518;753:23450;1:3113` |
| Table Cell | Varient=Header, Type=Text | Line 1 | stroke | #ECECEC → **Grey-200** | `66:1799` |
| Table Cell | Varient=Header, Type=Text | 번호 | fill | #B3B3B3 → **Grey-400** | `66:1797` |
| Toast Popup | State=Alert | Vector | stroke | #B3B3B3 → **Grey-400** | `I66:1689;66:2334;1:2583` |
| Toast Popup | State=Default | Vector | stroke | #B3B3B3 → **Grey-400** | `I66:1701;66:2334;1:2583` |
| Toast Popup | State=Error | Vector | stroke | #B3B3B3 → **Grey-400** | `I66:1695;66:2334;1:2583` |

소계: **37건** (distinct hex 기준 아래 집계)

| 현재값 | → 정본 토큰 | 건수 |
|---|---|---|
| #ECECEC | Grey-200 | 11 |
| #B3B3B3 | Grey-400 | 11 |
| #71717A | Grey-500 | 8 |
| #1A1A1A | Grey-800 | 2 |
| #FEFEFE | Grey-50 | 2 |
| #18181B | Grey-800 | 2 |
| #EF2E32 | Red-600 | 1 |

## B. 유지 — 로고 아트워크 (교정 안 함)

Signature 로고 고유 아트워크 색. UI 토큰 아님 → `tokens.css` 미포함, Figma에서도 유지.

| 컴포넌트 | variant | 레이어 | 속성 | 값 | 노드 ID |
|---|---|---|---|---|---|
| Signature | Sort=Signature, Color=Black | Vector | fill | #1D1D1B (로고) | `66:3931` |
| Signature | Sort=Signature, Color=Black | Vector | fill | #1D1D1B (로고) | `66:3932` |
| Signature | Sort=Signature, Color=Black | Vector | fill | #1D1D1B (로고) | `66:3933` |
| Signature | Sort=Signature, Color=Black | Vector | fill | #1D1D1B (로고) | `66:3934` |
| Signature | Sort=Signature, Color=Black | Vector | fill | #1D1D1B (로고) | `66:3935` |

## C. 유지 — 컴포넌트 로컬 확장색 (교정 안 함)

Tag Green/Yellow(`#38BA77`/`#E7F6E7`/`#E8C32E`/`#FCF7DF`)·Toast Alert(`#F5CA1D`). 근사 토큰 없음 → Foundation 확장색으로 명시 유지. 해당 컴포넌트 안에서만 허용.

## D. 무시 — Figma 컴포넌트셋 chrome (색 아님)

컴포넌트셋 프레임의 Figma 기본 보더/배경(선택 표시용). 실제 디자인 색이 아니므로 교정 대상 아님.

| 컴포넌트 | 레이어 | 속성 | 값 | 노드 ID |
|---|---|---|---|---|
| Attention | Attention | fill | #F9F4FF | `66:4004` |
| Attention | Attention | stroke | #8A38F5 | `66:4004` |
| Carousel | Carousel | stroke | #8A38F5 | `69:9181` |
| Signature | Signature | fill | #F9F4FF | `66:3929` |
| Signature | Signature | stroke | #8A38F5 | `66:3929` |

