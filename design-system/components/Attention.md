# Attention

- **노드 ID:** `66:4004` (COMPONENT_SET)
- **소속 페이지:** 1. Logo

## Variant 속성

- **Sort**: Attention
- **Color**: Black, White

## Variant 전체 (2)

| variant | 크기 | 텍스트 토큰 | 컬러(fill) | 보더(stroke) | 이펙트 |
|---|---|---|---|---|---|
| Sort=Attention, Color=Black | W×H 60×84 | — | Grey-900 (#000000) | — | — |
| Sort=Attention, Color=White | W×H 60×84 | — | Grey-50 (#FFFFFF) | — | — |

## 레이아웃 (오토레이아웃)

전 variant 공통 — 오토레이아웃 없음 — 자식은 절대좌표(자유배치)

## 하위 구조 (대표 variant, 2~3레벨)

`Sort=Attention, Color=Black` — 오토레이아웃 없음 — 자식은 절대좌표(자유배치)
- Vector (vector)

## Variant 차이 (무엇이 바뀌나)

- **Sort** (Attention) 변화 시 → 달라짐: **없음(동일 형태, 조합만 다름)** · 동일: 크기, 레이아웃, 텍스트, fill, stroke, 이펙트
- **Color** (Black / White) 변화 시 → 달라짐: **fill** · 동일: 크기, 레이아웃, 텍스트, stroke, 이펙트

## SVG 자산 (인라인)

파일: `assets/attention-black.svg`, `assets/attention-white.svg`. viewBox `60×84.3129` 단일 벡터.

**Black** (밝은 배경용):
```svg
<svg width="60" height="84.3129" viewBox="0 0 60 84.3129" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M60 0L0 15.5146V37.2516C0 37.7216 0.30934 38.1321 0.755503 38.2451L45.3896 49.7858L0 61.5289V84.3129L60 68.7983V47.1148C60 46.6449 59.6907 46.2344 59.2445 46.1214L14.5033 34.5509L60 22.7841V0Z" fill="black"/></svg>
```

**White** (어두운 배경용):
```svg
<svg width="60" height="84.3129" viewBox="0 0 60 84.3129" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M60 0L0 15.5146V37.2516C0 37.7216 0.30934 38.1321 0.755503 38.2451L45.3896 49.7858L0 61.5289V84.3129L60 68.7983V47.1148C60 46.6449 59.6907 46.2344 59.2445 46.1214L14.5033 34.5509L60 22.7841V0Z" fill="white"/></svg>
```

> White는 원본 결합 SVG에서 x-좌표 -180 평행이동(= Black과 동일 형상) 후 clipPath transform 제거. 전체 프레임 rect 클립은 불필요해 생략.

## 확인 필요

- 컬러/간격은 Figma **변수** 바인딩 → 값은 확정이나 변수 토큰명은 REST 미제공(위 값은 팔레트 매칭으로 표기).

