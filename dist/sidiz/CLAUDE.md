<!-- 자동 생성 파일 — 원본은 design-system/. 직접 수정 금지. -->
> **버전: 2026-08-21 / 생성 커밋: `c30def6`**
> 자동 생성 파일 — 원본은 `design-system/`. 직접 수정 금지.

> # ⚠️ 필수 — 생성물 저장 위치
> **모든 생성물(화면·HTML·목업 등)은 `~/Desktop/sidiz-output/`에 저장한다.** 폴더가 없으면 만든다.
> **작업 폴더·배포물 폴더 안에는 어떤 생성물도 만들지 않는다.** 추론·예외 없이 항상 적용한다.

> # ⚠️ 절대 원칙 — 정본 15색 · 14종 (예외 없음)
> 정본은 **컬러 15색(Blue 3 / Red 2 / Grey 10) + 타이포 14종**뿐이다. 정본 밖 색·크기·굵기는 쓰지 않는다(근사값·신규·중간 토큰 금지, 팔레트 확장 금지).
> **화면 제작 시 `tokens.css`의 클래스(타이포 14종 + 컴포넌트 클래스: `.btn-*`·`.table-header`·`.table-cell`·`.sidebar-item`·`.dashboard-card`·`.toast`·`.tag`·`.breadcrumb` 등)만 사용한다. `font-size`·`padding`·`height` 등을 직접 지정하지 않는다.** 필요한 클래스가 없으면 임의로 만들지 말고 관리자에게 알린다.
> 유일한 예외: 문서화된 **컴포넌트 로컬 확장색**(Tag Green/Yellow·Toast Alert)뿐 — 해당 컴포넌트 안에서만.

# SIDIZ 디자인 시스템 — 작업 지침 (Cowork)

이 폴더에서 UI가 포함된 결과물(화면·컴포넌트·스타일)을 만들거나 수정할 때, **같은 폴더의 `Design.md`(값·규격)와 `design-principles.md`(화면 조립·판단 기준)를 항상 참조하고, 그 규격·원칙대로 화면을 만든다.** 스타일은 `tokens.css`의 CSS 변수·조합 클래스로만 적용한다.

## 반드시 지킬 원칙

1. **정본 토큰·클래스만 사용한다.** 색·폰트·간격·radius는 `tokens.css`의 변수(`--sidiz-*`)와 클래스(타이포 `.title1`~`.caption5` + 컴포넌트 클래스 `.btn-*`·`.table-header`·`.table-cell`·`.sidebar-item`·`.dashboard-card`·`.toast`·`.tag`·`.breadcrumb` 등)로만 지정한다. **`font-size`·`padding`·`height`·임의 hex·radius를 직접 지정/발명하지 않는다.** 정본 밖 값(근사값 포함)은 쓰지 않는다. 필요한 클래스가 없으면 임의로 만들지 말고 관리자에게 알린다. **단, 문서화된 "컴포넌트 로컬 확장색"(Tag Green/Yellow·Toast Alert)은 해당 컴포넌트 클래스에 한해 허용**한다(전역 토큰 아님 → 다른 위치 사용 금지).

2. **폰트.** Pretendard 단일. 모든 텍스트 `line-height:150%`, `letter-spacing:1%`(토큰에 반영됨). Inter/Roboto/system 기본 폰트 금지.

3. **색.** 브랜드 포인트 `Blue-700 #003EFF`는 강조/선택/링크에만 **절제** 사용. 에러는 `Red-600`. 나머지는 Grey 10단계. 팔레트 밖 색(보라/초록/노랑/그라데이션) 금지.

4. **최소 크기 규칙.** Caption4·5(8·10px = `.caption4`/`.caption5`)는 **뱃지/태그/아이콘 라벨 전용**. 본문에 쓰지 않는다.

5. **구분은 border 우선.** 기본은 그림자 없이 hairline(`--sidiz-color-grey-200`)으로 구분한다. 그림자(`--sidiz-shadow-*`)는 떠 있는 표면(드롭다운/토스트/팝오버/카드 부양)에만. **앱·페이지 배경은 흰색(`--sidiz-color-grey-50`), 회색 채움 캔버스(`Grey-100` 등) 금지** — `Grey-100`은 테이블 헤더 등 지정 표면에만.

6. **radius.** 버튼/인풋 4~6px(`--sidiz-radius-4`/`-6`), 태그·칩·원형은 pill(`--sidiz-radius-pill`). 그 밖 임의 곡률 금지.

7. **컴포넌트.** 버튼·인풋·뱃지·탭·드롭다운 등은 `Design.md` 5장의 명세와 variant 범위 안에서만 사용한다. 한 화면의 "결정 버튼"은 하나로 제한한다.

8. **화면 조립.** 레이아웃·위계·패턴은 `design-principles.md`(원칙)와 `layouts.md`(화면 유형·공통 치수·조합 규칙)를 따른다. **아이콘은 `icons.md`**(Lucide 24×24·2px, 컴포넌트별 매핑) 기준으로만 쓰고 이모지 금지. **컴포넌트 방향·정렬은 `Design.md`의 오토레이아웃 요약을 지킨다**(Toast·Header는 SPACE_BETWEEN). 값=`Design.md`, 조립=`design-principles.md`/`layouts.md`.

## 값이 애매할 때

- `Design.md`에서 근거를 찾지 못하면 값을 지어내지 말고, 가장 가까운 정본 토큰을 쓰거나 사용자에게 확인한다.
- 이 배포본과 정본이 다르면 **정본(`design-system/`)이 우선**이다.
