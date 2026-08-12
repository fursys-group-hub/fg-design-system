<!-- 자동 생성 파일 — 원본은 design-system/. 직접 수정 금지. -->
<!-- 생성일: 2026-08-12 · 정본 덤프 기준 lastModified: 2026-08-12T07:05:46Z -->

# SIDIZ 디자인 시스템 배포본 — 사용법

SIDIZ 브랜드 규격(색·폰트·컴포넌트·레이아웃)대로 화면을 만들도록 돕는 배포 꾸러미입니다. 이 폴더에는 아래 파일이 있습니다.

| 파일 | 용도 |
|---|---|
| `design-system.md` | 사람·AI가 읽는 통합 규격서(값 + 사용 규칙) |
| `tokens.css` | 화면에 바로 링크해 쓰는 CSS 변수·클래스 |
| `CLAUDE.md` | Cowork/클로드 코드가 자동으로 따르는 작업 지침 |
| `README.md` | (이 문서) 사용법 |

---

## 쓰는 방법 (셋 중 택1)

### 1) 클로드 챗 (claude.ai)
1. 프로젝트를 하나 만듭니다.
2. **프로젝트 지식(Project knowledge)** 에 `design-system.md`를 업로드합니다.
3. "이 규격대로 ○○ 화면 만들어줘"라고 요청하면, 업로드한 규격을 따릅니다.

### 2) Cowork
1. 이 `dist/sidiz/` 폴더를 **작업 폴더로 지정**합니다.
2. 같은 폴더의 `CLAUDE.md`가 자동 적용되어, `design-system.md` 규격대로 작업합니다.
3. 별도 설정 없이 바로 UI 작업을 요청하면 됩니다.

### 3) 클로드 코드 (개발자)
1. 이 디자인 시스템 저장소를 **클론**합니다.
2. 작업 세션에서 `/sidiz-design-system` 스킬을 호출합니다.
3. 스킬이 규격을 로드한 상태로 UI를 생성·수정합니다.

---

## HTML에서 tokens.css 쓰기 (참고)

```html
<link rel="stylesheet" href="tokens.css" />
...
<h1 class="title3" style="color: var(--sidiz-color-grey-900)">페이지 제목</h1>
<button style="border-radius: var(--sidiz-radius-4); background: var(--sidiz-color-grey-900); color: var(--sidiz-color-grey-50)">확인</button>
```

- 텍스트는 `.title1`~`.caption5` 클래스로, 색·간격·radius는 `--sidiz-*` 변수로 지정합니다.
- 정본에 없는 임의 색·크기·radius는 쓰지 않습니다.

---

## 업데이트 받는 법

- 이 배포본은 **자동 생성물**입니다. 원본(source of truth)은 저장소의 `design-system/`입니다.
- 디자인이 바뀌면 정본을 갱신한 뒤 **다시 export** 해서 이 폴더의 파일을 통째로 교체하세요. (정본 → 배포물 **단방향**, 배포본을 직접 고치지 않습니다.)
- 최신 여부가 궁금하면 각 파일 상단 주석의 `생성일` / `정본 덤프 lastModified`를 확인하세요.
