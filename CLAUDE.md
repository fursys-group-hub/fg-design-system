# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **Repo state:** This git repo is currently empty (no commits, no tracked files). It is the intended git home for the **SIDIZ Design System Claude Code plugin**. The canonical plugin content currently lives outside this repo — see "Where the source lives" below — and should be brought into this repo and versioned here.

## 디자인 작업 지침 (필수)

디자인 기준의 원본(source of truth)은 `design-system/` 폴더이며, 모든 디자인 관련 작업 전에 `design-system/index.md`를 먼저 읽는다.

## 디자인 시스템 문서 작성 원칙 (필수)

`design-system/` 아래 문서를 작성·수정할 때 아래 원칙을 반드시 지킨다.

- **원본 형식은 마크다운.** 토큰 기준서는 `design-system/tokens/` 아래 마크다운 문서다(`color.md`, `typography.md`, `spacing.md`). `tokens.css` 같은 코드 형식 파일은 지금 만들지 않는다. 필요해지면 이 마크다운 문서에서 변환해 생성한다.
- **토큰 항목 형식:** 각 토큰은 `토큰 이름 / 값 / 용도 / 사용 규칙(언제 쓰고, 언제 쓰면 안 되는지)`를 갖춘다.
- **추측 금지.** Figma에서 아직 못 읽었거나 확실하지 않은 값은 절대 추측하지 말고 `[확인 필요]`로 표시한다. 값을 지어내지 않는다.
- **파일 길이 제한.** 각 문서는 500줄을 넘지 않는다. 넘으면 파일을 쪼갠다.

## What this project is

This is **not an app**. It is a Claude Code **plugin/skill** that makes Claude follow the SIDIZ (시디즈) brand design system (colors, typography, components, layout) whenever it generates or edits UI. It is distributed either by copying the skill folder or via an internal plugin marketplace (`/plugin marketplace add <git repo>` → `/plugin install sidiz-design-system`). Source of truth for the design tokens themselves is the Figma file `시디즈닷컴_디자인에셋_SIDIZ`.

## Where the source lives (critical)

The plugin exists in **two locations that must be kept in sync** — editing only one does not take effect:

- **Deployment origin** (team distribution / reinstall): `/Users/su/Downloads/files (1)/sidiz-design-system`
- **Active skill** (where Claude actually loads it): `~/.claude/skills/sidiz-design-system/skills/sidiz-design-system`

If you change the design system, apply the identical change to **both** locations (and, once populated, to this repo). Changing only the origin will not be reflected in the next session.

## Plugin structure

```
sidiz-design-system/
├── .claude-plugin/plugin.json          # Plugin manifest (name, version, author)
├── skills/sidiz-design-system/
│   ├── SKILL.md                        # Core rules + auto-trigger conditions
│   ├── references/
│   │   ├── colors.md                   # Palette (basic / system / semantic)
│   │   ├── typography.md               # Type scale title1~caption2
│   │   ├── components.md               # Button / input / badge / tab / filter specs
│   │   ├── layout.md                   # Breakpoints / spacing / popup / snackbar
│   │   └── admin-dashboard.md          # Admin / dashboard / internal-tool screens
│   └── assets/
│       ├── tokens.css                  # CSS variables + component classes (copy into projects)
│       ├── admin-dashboard.css         # Admin scaffold styles (link alongside tokens.css)
│       └── starter-example.html        # Applied example
├── CLAUDE.md.snippet                   # Paste into a consuming project's CLAUDE.md
└── README.md
```

`SKILL.md` is the authoritative spec; `references/*.md` are detailed extensions loaded on demand; `assets/*.css` are the shippable token/class files that consuming projects copy in and link.

## Design rules this plugin enforces

When doing any UI work (this repo's examples, or any consuming project), load the `sidiz-design-system` skill first and follow `SKILL.md`. Key non-negotiables:

- **Colors:** only brand point color is SIDIZ Blue `#003EFF`; neutrals from gray 000–900; error `#FF3A4A`. No purple/green/gradients ("AI-style" palettes are banned). Use only `tokens.css` CSS variables — never invent values.
- **Fonts:** Korean = Pretendard, Latin/numerals = Centra No.2 (fallback Pretendard). Body `letter-spacing: -0.02em`. No Inter/Roboto/system defaults.
- **Radius:** buttons/inputs 4px; icon frames 4–6px; filters/badges/color-chips = pill (9999px). No other values; no 12–24px radius on large cards.
- **Buttons:** one "decision button" per page (black bg / white text, H54); primary = white bg + border, H34. Blue fill buttons are not the default.
- **Elevation:** no shadows by default — separate with borders (`--border-basic1~3`).
- **Anti-AI-cliché:** no accent rails/color bars on cards, no `·`/`•` separators (use `/`), no emoji icons (1px stroke only), no nested "box-in-box" cards, no large status-color fills, no glassmorphism/gradients/uniform 3-KPI tiles, no bold titles. Express hierarchy with whitespace, hairlines, and restrained point color.
- **Admin / dashboard / internal / data-entry screens** follow `references/admin-dashboard.md` + `admin-dashboard.css`: white header/sidebar (no dark/navy), left white icon rail + sticky top bar over a `gray-100` canvas with white cards, symbol mark logo (never "SIDIZ" wordmark), compact inputs H44 (`--input-h-admin`, vs commerce default H50), plain-text section titles, right-aligned field-status pills, `.segmented` toggles, full-width save button.

The full rule table and rationale live in `SKILL.md` — read it before generating UI rather than relying on this summary.

## Maintenance workflow

1. Edit the Figma source of truth, then reflect changes in `tokens.css` / `references/*.md`.
2. Apply the change to **both** locations listed under "Where the source lives" (and this repo).
3. Bump `version` in `.claude-plugin/plugin.json` and publish so marketplace installs update.
