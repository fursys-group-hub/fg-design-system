# Icons — SIDIZ 아이콘 세트

정본: Figma `퍼시스그룹_디자인 시스템` `4. Icons` 페이지 (아이콘 인스턴스 1469종).

## 세트 규격

| 항목 | 값 | 규칙 |
|---|---|---|
| 세트 | **Lucide** (`lucide.dev`) | 오픈소스 아이콘. 전체 1469종 사용 가능 |
| 크기 | **24×24** | 기본 프레임 24×24. 축소 시 비율 유지 |
| stroke | **1.2** | 컴포넌트 안 모든 아이콘 stroke 1.2 단일(예외 없음). 전역 `svg{stroke-width:1.2}`로 적용하고 개별 재지정 금지. 채움(fill) 아이콘 예외 |
| 이름 규칙 | `Icon / <PascalCase>` | Figma 인스턴스명 = Lucide 아이콘명 PascalCase (예: `Icon / ChevronDown` = Lucide `chevron-down`) |
| 색 | `currentColor` 권장 | 색은 팔레트 토큰으로: 기본 `Grey-900`/무채색, 상태 아이콘은 상태색(경고=`Red-600`, 포인트(완료)=`Blue-600`). 임의 색 금지 |

- **이모지 아이콘 금지.** 아이콘은 반드시 위 Lucide SVG(24×24 프레임·**stroke 1.2**)로 렌더한다.
- 아이콘 원본 SVG는 `lucide.dev`에서 이름으로 받아 그대로 사용한다(별도 자산 파일 미보관).

## 컴포넌트별 사용 아이콘 (매핑)

각 컴포넌트가 실제 참조하는 아이콘(정본 `3. Component` 하위 구조 기준).

| 컴포넌트 | 사용 아이콘 (Lucide) |
|---|---|
| Button | `Plus`, `Search` |
| Input | `Calendar`, `ChevronDown`, `ChevronUp`, `Search` |
| Input Case | `CircleAlert` |
| Checkbox | `Check`, `Minus` |
| Dropdown List | `ChevronDown`, `LogOut`, `Search`, `Settings` |
| Search Filter | `Calendar`, `ChevronDown`, `ChevronUp`, `Minus`, `Plus`, `Search` |
| Tab | `Sun` |
| Table Cell | `Plus`, `Trash2` |
| Toast Popup | `Check`, `CircleAlertFill`, `Plus`, `X` |
| Carousel | `ChevronLeft`, `ChevronRight` |
| Sidebar | `BarChartBig`, `Calculator`, `ChevronDown`, `ClipboardList`, `ClipboardPen`, `FolderSearch`, `Layers3`, `LayoutDashboard`, `MessageSquareText`, `Package`, `ScrollText`, `Search`, `Settings`, `Volume2` |
| Breadcrumb | `ChevronRight` |
| Header | `Bell`, `ChevronDown`, `PanelLeft` |
| Pagination | `ChevronLeft`, `ChevronRight` |

**컴포넌트가 참조하는 고유 아이콘 29종:**
`BarChartBig · Bell · Calculator · Calendar · Check · ChevronDown · ChevronLeft · ChevronRight · ChevronUp · CircleAlert · CircleAlertFill · ClipboardList · ClipboardPen · FolderSearch · Layers3 · LayoutDashboard · LogOut · MessageSquareText · Minus · Package · PanelLeft · Plus · ScrollText · Search · Settings · Sun · Trash2 · Volume2 · X`

## 그 외 아이콘

위 29종 외에도 **Lucide 전체 세트(1469종)를 사용할 수 있다.** 필요한 아이콘은 `lucide.dev`에서 이름으로 찾아 동일한 PascalCase(`Icon / <Name>`)로 사용한다. 세트 밖(다른 아이콘 라이브러리·이모지)은 쓰지 않는다.

## 확인 필요

- `CircleAlertFill` — Lucide 표준 `CircleAlert`의 **채움(fill) 변형**(Toast Alert·경고 표시용). 표준 stroke 버전(`CircleAlert`)은 Input Case에서 사용. 두 형태 구분해 적용.
