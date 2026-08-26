<!-- SIDIZ 디자인 시스템 작업 지침 — 2026-08-21 전면 개정 (v5) -->
<!-- 이 파일이 최신 정본이다. 이전 버전의 지침 문구와 충돌하면 이 파일을 따른다. -->

# 최우선 원칙 — HTML 을 새로 작성하지 않는다

화면이나 컴포넌트를 만들 때 **마크업을 스스로 작성하지 않는다.**
`COMPONENTS.html` 의 마크업을 **그대로 복사해서 조립**하고 **텍스트 내용만** 교체한다.

- 구조, 클래스명, 중첩 순서, 아이콘 위치를 바꾸지 않는다.
- `COMPONENTS.html` 에 없는 구조가 필요하면 **임의로 만들지 않고 관리자에게 보고**한다.
- 스타일은 `sidiz-components.css` 와 `tokens.css` 의 클래스만 쓴다.
  `font-size`, `padding`, `height`, `stroke-width`, hex 색을 직접 지정하지 않는다.
  `width` 지정만 예외로 허용한다.

이 원칙 없이 산문 설명만 읽고 HTML 을 새로 쓰면 생성마다 결과가 달라진다.
실제로 그 문제가 반복되어 이 규칙이 생겼다.

# 파일 우선순위

| 순위 | 파일 | 역할 |
|---|---|---|
| 1 | `COMPONENTS.html` | **마크업 정본.** 복사해서 조립할 원본 |
| 2 | `sidiz-components.css` | **컴포넌트 CSS 정본.** 피그마 실측. 수정 금지 |
| 3 | `tokens.css` | 색과 타이포 변수, 타이포 클래스 |
| 4 | `component-spec.md` | 피그마 실측 수치 원장. 근거 확인용 |
| 5 | `layouts.md` | 화면 유형별 골격과 배치 순서 |
| 6 | `design-principles.md` | 판단 기준 |

값이 서로 다르면 위 순번이 낮은 쪽(숫자가 작은 쪽)을 따른다.

# 절대 지우면 안 되는 CSS 두 블록

## 1. 폰트 스무딩

```
html, body {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```

이 블록이 없으면 macOS 브라우저가 서브픽셀 안티에일리어싱으로 글자를 굵게 그린다.
피그마보다 굵어 보이는 문제의 원인이 이것이다. 특히 어두운 배경 위 흰 글자에서 심하다.

## 2. 아이콘 stroke

```
svg { stroke-width: 1.2; }
```

Lucide 기본값은 2 라서 이 줄이 없으면 모든 아이콘이 굵어진다.

# 아이콘 규칙

**컴포넌트 안의 모든 아이콘은 stroke 1.2 단일이다. 예외 없다.**

피그마 원본에는 1.0 부터 2.4 까지 흩어진 값이 있으나 이는 24px 마스터를 축소할 때 생긴
스케일 잔재다. 실측 106개 중 62개가 1.2 이고 정본 규칙도 1.2 다.
개별 컴포넌트에서 `stroke-width` 를 다시 지정하지 않는다.

크기는 기본 16, Header 의 PanelLeft 와 Bell 은 20, Breadcrumb 과 Button Flat/Text 안은 12,
Checkbox 안은 11 이다.

색은 인풋 계열 Grey-400, 사이드바 메뉴 Grey-900(활성 Primary-600),
Header PanelLeft 와 Bell 은 Grey-900, 버튼 안은 버튼 글자색을 따른다. 이모지 금지.

# 색

정본은 **22색**뿐이다: **Primary 2톤(브랜드별) + System 10(공통) + Grey Scale 10(공통).**
Primary 는 **9개 브랜드마다 다르며 600/200 두 톤**만 쓴다. System·Grey 는 9브랜드 공통이다.

**Primary (브랜드별 · 기본 그룹사 공통)**
Primary-600 `#6725F3` — 브랜드 포인트: 버튼 배경·사이드바 활성·라인탭 밑줄·섹션 건수
Primary-200 `#F0E9FE` — 브랜드 강조 배경: 사이드바 활성 배경

**System (9브랜드 공통 · 각 600/100)**
Red 600 `#EF2E32` / 100 `#FBE7E7` · Yellow 600 `#D4A300` / 100 `#F9F1D9` · Green 600 `#2AA75E` / 100 `#DFF2E7`
Blue 600 `#3769DE` / 100 `#EBF0FC` · Gray 600 `#909090` / 100 `#F0F0F0`

**Grey Scale (10 · 공통)**
Grey 900 `#000000` / 800 `#242526` / 700 `#434548` / 600 `#595C5E` / 500 `#7C8084`
Grey 400 `#A4AAB0` / 300 `#D6DADE` / 200 `#EAEDF0` / 100 `#F5F6F7` / 50 `#FFFFFF`

## 브랜드별 Primary (9)

`<html data-brand="...">` 로 전환한다. 미지정 시 기본은 그룹사 공통.

| 브랜드 한글명 | 슬러그 | Primary-600 | Primary-200 |
|---|---|---|---|
| 시디즈 | `sidiz` | `#003EFF` | `#E3EDFF` |
| 퍼시스 | `fursys` | `#E3001C` | `#FCE5E8` |
| 일룸 | `iloom` | `#D60707` | `#FEDADA` |
| 데스커 | `desker` | `#272727` | `#E9E9E9` |
| 알로소 | `alloso` | `#B14E3F` | `#F7EDEC` |
| 슬로우베드 | `slowbed` | `#0D207C` | `#D7E4F0` |
| 레터스 | `letus` | `#FF5C39` | `#FFF3ED` |
| 퍼플식스 | `purplesix` | `#7800F5` | `#F4E8FF` |
| 그룹사 공통(기본) | `group` | `#6725F3` | `#F0E9FE` |

상태 색: 완료=System `Blue-600`, 진행중=`Green-600`, 보류=`Yellow-600`, 취소/실패=`Red-600`.
**옛 로컬 확장색(Tag Green/Yellow·Toast Alert)은 System 으로 편입되어 사라졌다.**
Primary-600 은 강조·선택·링크·건수 표기에만 절제해서 쓴다.

# 타이포

Pretendard 단일. 모든 텍스트 `line-height: 150%`, `letter-spacing: 1%`.
정본 14종만 쓴다.

Title1 40/600 · Title2 26/600 · Title3 22/600 · Title4 16/600 · Title5 14/600
Body1 13/600 · Body2 13/400 · Body3 12/600 · Body4 12/400
Caption1 11/600 · Caption2 10/600 · Caption3 10/400 · Caption4 8/600 · Caption5 8/400

## 컴포넌트별 확정 크기 (피그마 전수 실측)

| 위치 | 크기와 굵기 |
|---|---|
| 페이지 타이틀 | Title4 16/600 Grey-900 |
| 페이지 타이틀 우측 서브 문구 | Body4 12/400 Grey-400, baseline 정렬, gap8, 서술형은 마침표로 끝낸다 |
| 섹션 타이틀 | Title5 14/600 Grey-900 |
| 섹션 건수 | Title5 14/600 Primary-600, gap4, **단위를 붙이지 않는다** |
| Table 헤더 | Caption1 11/600 Grey-400 |
| Table 셀 | Body2 13/400 Grey-900 |
| Input placeholder 와 입력값 | Body2 13/400 (Stepper 만 Body4 12/400) |
| Input Case 라벨 (단독) | Body3 12/600 Grey-500 |
| Input Case 라벨 (필터 카드 안) | Caption1 11/600 Grey-500 |
| Button Square, Round | Body1 13/600 |
| Button Flat, Text | Body3 12/600 |
| Tag 12변형 전부 | Caption1 11/600 |
| Dashboard Card 수치 | Title3 22/600 |
| Dashboard Card 단위 | Caption1 11/600 |
| Sidebar 메뉴 항목 | Body1 13/600 |
| Sidebar 시스템명 | Title5 14/600 |
| Header 담당자명 | Body1 13/600 |
| Header 역할 뱃지 | Caption1 11/600 Grey-400 |
| Tab Line | Title5 14/600 |
| Tab Box | Body1 13/600 |
| Toast 본문 | Body1 13/600 Grey-50 |
| Toast 닫기 | Body2 13/400 Grey-400 |
| Breadcrumb | Body2 13/400 Grey-400, 현재 위치만 Body1 13/600 Grey-900 |
| Pagination | 현재 Body1 13/600 Grey-900, 나머지 Body2 13/400 Grey-400 |
| Dropdown 항목 | Body2 13/400 Grey-900 |
| Dropdown 담당자명 | Title5 14/600 |

# 상태 태그 5범주 매핑

5범주는 **색을 고르는 분류 기준**이다. **라벨 텍스트는 업무 용어를 그대로 쓴다.**
결제완료를 완료로 바꾸지 않는다. 배송중을 진행중으로 바꾸지 않는다.

| 범주 | 포함 예 | 요약 카드 | 테이블 안 |
|---|---|---|---|
| 대기 | 접수, 승인 대기, 요청 대기 | `black-light` | `black-light` |
| 보류 | 배송준비, 중지, 확인 필요 | `yellow-light` | `yellow-light` |
| 진행중 | 배송중, 처리중, 입고 진행, 조치중 | `green-light` | `green-light` |
| 완료 | 결제완료, 승인, 입고 완료, 매핑 완료 | `blue-light` | `blue-light` |
| 취소/실패 | 취소, 실패, 반려, 오류, 미매핑 | `red-dark` | `red-light` |

취소와 실패만 위치에 따라 다르다. 요약 카드는 강조가 필요해 dark,
행이 많은 테이블은 시각 부담을 줄여 light 를 쓴다. 나머지 4범주는 위치에 관계없이 동일하다.

새 상태값은 반드시 위 5범주 중 의미가 가장 가까운 곳에 넣는다. 6번째 색을 만들지 않는다.

**Dashboard Card 의 수치와 단위 글자색은 그 카드 태그의 진한 색과 같게 맞춘다.**
카드에 `sidiz-card--wait` / `--hold` / `--progress` / `--done` / `--fail` 중 하나를 붙이면 자동 적용된다.

# Search Filter 구조

한 행 안에 필드 컨테이너와 버튼 그룹이 나란히 있다. 버튼은 하단 정렬이다.

- 필드 폭은 **가변 분배**다. 피그마에 적힌 166 이나 348 은 fill 분배의 결과값이므로 고정하지 않는다.
- 기간 필드만 고정이다. 프리셋 드롭다운 136 + gap4 + 날짜 범위 인풋 216.
- 날짜 범위 인풋은 `0000/00/00 - 0000/00/00` 을 한 줄로 유지한다. 날짜 인풋 2개로 쪼개지 않는다.
- 필드가 한 줄에 안 들어가면 **필드만** 다음 줄로 넘어간다. 버튼은 항상 마지막 줄 오른쪽에 남는다.
- 조회 버튼은 **Secondary Round**(흰 배경 + Grey-200 보더)다. Primary 검정이 아니다.
- 상세 조회는 **Text**(투명 배경)다. 아이콘은 Default 에서 Plus, Extended 에서 Minus.
- 접기 토글은 카드 하단 중앙에 24 원형이다.

# Table 구조

- **No. 열을 두지 않는다.** 첫 열은 체크박스 열(폭 48)이다.
- **테이블 전체를 Grey-200 외곽선 + radius 4 로 감싼다.** `sidiz-table-wrap` 으로 감싸며,
  마지막 행의 하단 보더는 제거한다. 외곽선을 빼면 표가 배경에 떠 보인다.
- 헤더 H32 Grey-100 배경, 셀 H38, 좌우 padding 16, 행 구분은 Grey-200 hairline.
- 링크와 URL 은 밑줄, 색은 Grey-900.
- 테이블은 컨테이너 폭에 맞춰 늘어난다. 콘텐츠 폭 기준은 1280.
- 페이지네이션은 **테이블 가로 폭 기준 중앙 정렬**이다. `sidiz-pagination-wrap` 으로 감싼다.

# Toast

- 상태 아이콘은 24 원 안에 12px 글리프다.
- Default 는 체크, Error 는 X, **Alert 는 느낌표만** 넣는다. 원형 라인이 있는 아이콘을 쓰면
  원 안에 원이 겹쳐 보인다.
- 우측은 닫기 텍스트 버튼만 둔다. X 나 Plus 아이콘을 넣지 않는다.

# Checkbox 5상태

| 상태 | 클래스 | 박스 |
|---|---|---|
| Unchecked | (없음) | 흰 배경 + Grey-300 보더 |
| Hover | (CSS `:hover`) | 흰 배경 + Grey-900 보더 |
| Checked | `is-checked` | Grey-900 배경 + 흰 체크 |
| Multiple Checked | `is-multiple` | 흰 배경 + Grey-900 보더 + Grey-900 체크 |
| Disabled | `is-disabled` | Grey-300 배경 + 흰 마이너스, 클릭 불가 |

16 프레임 안에 13 박스(r2), 체크와 마이너스 글리프는 11px 이다.
마크업에는 체크와 마이너스 두 아이콘을 항상 넣고 표시는 CSS 가 제어한다.

**클릭 토글 동작이 필요하다.** 테이블 헤더의 체크박스는 전체 선택과 해제로 동작하고,
일부만 선택된 상태에서는 헤더가 `is-multiple` 로 바뀐다.
`COMPONENTS.html` 하단의 토글 스크립트를 그대로 복사해 쓴다.

# Tab

- Line 형에는 **아이콘을 넣지 않는다.**
- 선택 탭은 하단 Primary-600 2px + 투명 배경 + shadow-sm, 글자 Grey-900. 미선택은 Grey-300.
- Box 형은 컨테이너 r6 padding4 Grey-100, 선택 r4 흰 배경 shadow-sm, 미선택 r2.

# 화면 레이아웃 규칙

| 항목 | 값 |
|---|---|
| 전체 화면 폭 | 1600 |
| Sidebar 폭 | 256 (고정, 좌우 padding 12) |
| 본문 영역 폭 | 1344 (= 1600 - 256) |
| Contents padding | 상24 좌우32 하100 |
| 콘텐츠 폭 | **1280** (= 1344 - 64). 본문 안의 모든 컴포넌트는 1280 안으로 들어온다 |
| 본문 배경 | **Grey-100** |
| 콘텐츠 카드 표면 | Grey-50 (흰색) + Grey-200 보더 |
| 기본 그룹 간격 | 32 |
| 섹션 타이틀 다음 | 8 |
| 탭(Line) 다음 | 8 |
| 표와 페이지네이션 사이 | 16 |
| Dashboard Card 한 줄 개수 | 최대 4개, 5번째부터 다음 줄, 폭은 균등 분배 |

화면이 1600 보다 넓어지면 콘텐츠는 1280 을 유지하고 **좌우 여백만 균등하게** 늘어난다.
`sidiz-container` 가 `max-width: 1280px; margin: 0 auto` 로 이 규칙을 담당한다.

골격 클래스는 `sidiz-app` → `sidiz-sidebar` + `sidiz-main`(`sidiz-header` + `sidiz-contents` → `sidiz-container`) 이다.

## 조립 순서

1. Sidebar 폭 256, 항목 H34, 검색 H38, 로고 18x25.3
2. Header 높이 50, 좌우 padding 24, 하단 Grey-200 보더
3. Contents 배경 Grey-100, padding 상24 좌우32 하100
4. Container 폭 1280 중앙 정렬
5. 페이지 타이틀 블록 → 필터 카드 → 요약 카드 행 → 섹션 타이틀과 건수 → 목록 테이블 → 페이지네이션
6. Floating 레이어(드롭다운, 토스트)

# 생성물 저장 위치

모든 생성물은 `~/Desktop/sidiz-output/` 에 저장한다. 폴더가 없으면 만든다.
저장소 폴더와 배포물 폴더 안에는 어떤 생성물도 만들지 않는다.

# 값이 애매할 때

`COMPONENTS.html` 에서 근거를 찾지 못하면 값을 지어내지 말고 관리자에게 확인한다.
가장 가까운 값으로 근사하지 않는다. 근사가 누적되면 정본과 벌어진다.
