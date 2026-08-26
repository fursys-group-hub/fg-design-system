> ⚠️ 이 파일은 피그마 실측 기록이다. 색 이름은 2026-08-26 구조 개편 이전 기준이며, sync 가 변수 모드를 읽게 되면 자동으로 갱신된다. 수기로 고치지 않는다.

# SIDIZ 컴포넌트 상세 스펙 v2 (피그마 실측, 인스턴스 오버라이드 해석 포함)

표기: 색은 토큰명(실측 hex). LIB! 표시는 외부 라이브러리 변수 바인딩(재바인딩 대상). @(x,y)는 부모 기준 절대 위치.


## Pagination

### Pagination
- Pagination | 176x20 | 가로 gap12 pad(0,0,0,0) 정렬 시작/중앙
  - 아이콘 ChevronLeft 16x16, stroke 1.2, 색 Grey-900(#000000)
  - 숫자 | 120x20 | 가로 gap20 pad(0,0,0,0) 정렬 중앙/중앙
    - 1 | 6x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '1'
    - 2 | 8x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '2'
    - 3 | 9x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '3'
    - 4 | 9x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '4'
    - 5 | 8x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '5'
  - 아이콘 ChevronRight 16x16, stroke 1.2, 색 Grey-900(#000000)

## Carousel

### Varient=Indicator
- Varient=Indicator | 168x6 | 가로 gap12 pad(0,0,0,0) 정렬 중앙/중앙
  - Ellipse 22 | 6x6 | 배경 Grey-50(#FFFFFF)
  - Ellipse 23 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 24 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 25 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 26 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 27 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 28 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 29 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 30 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)
  - Ellipse 31 | 6x6 | 배경 Grey-50(#FFFFFF@0.30)

### Varient=Navigator
- Varient=Navigator | 80x30 | 가로 gap20 pad(0,0,0,0) 정렬 시작/중앙
  - Frame 1000007733 | 30x30 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF@0.70)
    - 아이콘 ChevronLeft 16x16, stroke 1.8, 색 Grey-900(#000000)
    - Rectangle 3962 [숨김] | 5.09117x10.1823 | 보더 Gray/Gray-900(#1A1A1A) LIB! (전체 1.2px, INSIDE)
  - Frame 1000007732 | 30x30 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF@0.70)
    - 아이콘 ChevronRight 16x16, stroke 1.8, 색 Grey-900(#000000)
    - Rectangle 3962 [숨김] | 5.09117x10.1823 | 보더 Gray/Gray-900(#1A1A1A) LIB! (전체 1.2px, INSIDE)

## Tab

### Varient=Line
- Varient=Line | 570x40 | 가로 gap0 pad(0,0,0,0) 정렬 시작/시작 | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Select | 114x40 | 가로 gap8 pad(8,0,8,0) 정렬 중앙/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Blue-700(#003EFF) (하 2px, INSIDE) | 그림자 DROP(0,1,2,0)#000000@0.05
    - 아이콘 Sun 16x16, stroke 1.33, 색 마스터 상속 [숨김]
    - 선택 메뉴명 | 65x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '선택 메뉴명'
    - 100 | 25x21 | 색 Grey-400(#A4AAB0) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '100'
  - Default | 114x40 | 가로 gap8 pad(8,0,8,0) 정렬 중앙/중앙 | 인스턴스: Active=Off
  - Default | 114x40 | 가로 gap8 pad(8,0,8,0) 정렬 중앙/중앙 | 인스턴스: Active=Off
  - Default | 114x40 | 가로 gap8 pad(8,0,8,0) 정렬 중앙/중앙 | 인스턴스: Active=Off
  - Default | 114x40 | 가로 gap8 pad(8,0,8,0) 정렬 중앙/중앙 | 인스턴스: Active=Off

### Varient=Box
- Varient=Box | 608x40 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작
  - Menu | 608x40 | 가로 gap0 pad(4,4,4,4) 정렬 시작/중앙 | r6 | 배경 Grey-100(#F5F6F7)
    - Select | 120x33 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 그림자 DROP(0,1,2,0)#000000@0.05 | 인스턴스: Active=On
    - Default | 120x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2 | 인스턴스: Active=Off
    - Default | 120x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2 | 인스턴스: Active=Off
    - Default | 120x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2 | 인스턴스: Active=Off
    - Default | 120x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2 | 인스턴스: Active=Off

## Toast Popup

### State=Alert
- State=Alert | 520x56 | 가로 gap100 pad(32,12,32,12) 정렬 양끝(SB)/중앙 | r6 | 배경 Grey-900(#000000) | 그림자 DROP(0,4,6,-2)#000000@0.05;DROP(0,10,15,-3)#000000@0.10
  - Frame 1000007709 | 276x24 | 가로 gap16 pad(0,0,0,0) 정렬 중앙/중앙
    - Icon / CircleAlertFill | 24x24 | 자유배치
      - Frame 4185 | 24x24 | 자유배치 | 위치 (0.0,0.0)
        - Ellipse 3 | 24x24 | 배경 AlertYellow(#F5CA1D) | 위치 (0.0,0.0)
        - Vector | 0.0119998x9.6 | 보더 Grey-50(#FFFFFF) (전체 1.2px, CENTER) | 위치 (12.0,7.2)
    - 최초 로그인 시 비밀번호 재설정이 필요합니다. | 236x20 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '최초 로그인 시 비밀번호 재설정이 필요합니다'
  - Button | 47x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 인스턴스: Varient=Secondary, Shape=Text

### State=Error
- State=Error | 520x56 | 가로 gap100 pad(32,12,32,12) 정렬 양끝(SB)/중앙 | r6 | 배경 Grey-900(#000000) | 그림자 DROP(0,4,6,-2)#000000@0.05;DROP(0,10,15,-3)#000000@0.10
  - Frame 1000007709 | 294x24 | 가로 gap16 pad(0,0,0,0) 정렬 중앙/중앙
    - Frame 1000007710 | 24x24 | 자유배치 | r9999 | 배경 Red-600(#FF3A4A)
      - 아이콘 X 12x12, stroke 2.4, 색 Grey-50(#FFFFFF) @(6.0,6.0)
    - 등록에 실패했습니다. 잠시 후 다시 시도해 주세요. | 254x20 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '등록에 실패했습니다. 잠시 후 다시 시도해 '
  - Button | 47x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 인스턴스: Varient=Secondary, Shape=Text

### State=Default
- State=Default | 520x56 | 가로 gap100 pad(32,12,32,12) 정렬 양끝(SB)/중앙 | r6 | 배경 Grey-900(#000000) | 그림자 DROP(0,4,6,-2)#000000@0.05;DROP(0,10,15,-3)#000000@0.10
  - Frame 1000007708 | 270x24 | 가로 gap16 pad(0,0,0,0) 정렬 중앙/중앙
    - Frame 1000007710 | 24x24 | 자유배치 | r9999 | 배경 Blue-500(#357FFF)
      - 아이콘 Check 12x12, stroke 2.4, 색 Grey-50(#FFFFFF) @(6.0,6.0)
    - 선택하신 주문이 정상적으로 등록되었습니다. | 230x20 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '선택하신 주문이 정상적으로 등록되었습니다.'
  - Button | 47x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 인스턴스: Varient=Secondary, Shape=Text

## Dashboard Card

### Dashboard Card
- Dashboard Card | 314x65 | 가로 gap0 pad(20,16,20,16) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Tag | 28x18 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: State=Light, Color=Black
  - Frame 4192 | 246x33 | 가로 gap4 pad(0,0,0,0) 정렬 끝/끝
    - 100 | 39x33 | 색 Grey-900(#000000) | 텍스트 Title/Title3-SemiBold (SemiBold 22) | 내용 '100'
    - Frame 1000007756 | 11x22 | 세로 gap0 pad(0,0,0,5) 정렬 중앙/중앙
      - 건 | 11x17 | 색 Grey-900(#000000) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '건'

## Breadcrumb

### Breadcrumb
- Breadcrumb | 308x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
  - 메뉴명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '메뉴명'
  - 아이콘 ChevronRight 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 메뉴명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '메뉴명'
  - 아이콘 ChevronRight 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 메뉴명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '메뉴명'
  - 아이콘 ChevronRight 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 메뉴명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '메뉴명'
  - 아이콘 ChevronRight 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 현재 메뉴명 | 60x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '현재 메뉴명'

## Radio

### State=Hover
- State=Hover | 16x16 | 자유배치
  - Radio | 14x14 | 자유배치 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 위치 (1.0,1.0)

### State=Inactive
- State=Inactive | 16x16 | 자유배치
  - Radio | 14x14 | 자유배치 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE) | 위치 (1.0,1.0)

### State=Activated
- State=Activated | 16x16 | 자유배치
  - Radio | 14x14 | 자유배치 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 위치 (1.0,1.0)
    - Ellipse 1 | 9x9 | 배경 Grey-900(#000000) | 위치 (2.5,2.5)

## Check Box

### State=Hover
- State=Hover | 16x16 | 자유배치
  - Frame 1000007700 | 13x13 | 자유배치 | r2 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 위치 (1.5,1.5)

### State=Disabled
- State=Disabled | 16x16 | 자유배치
  - Frame 1000007700 | 13x13 | 자유배치 | r2 | 배경 Grey-300(#D6DADE) | 위치 (1.5,1.5)
    - 아이콘 Minus 11x11, stroke 2.18, 색 Grey-50(#FFFFFF) @(1.0,1.0)

### State=Multiple Checked
- State=Multiple Checked | 16x16 | 자유배치
  - Frame 1000007700 | 13x13 | 자유배치 | r2 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 위치 (1.5,1.5)
    - 아이콘 Check 11x11, stroke 2.18, 색 Grey-900(#000000) @(1.0,1.0)

### State=Unchecked
- State=Unchecked | 16x16 | 자유배치
  - Frame 1000007700 | 13x13 | 자유배치 | r2 | 배경 Grey-50(#FFFFFF) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE) | 위치 (1.5,1.5)

### State=Checked
- State=Checked | 16x16 | 자유배치
  - Frame 1000007699 | 13x13 | 자유배치 | r2 | 배경 Grey-900(#000000) | 위치 (1.5,1.5)
    - 아이콘 Check 11x11, stroke 2.18, 색 Grey-50(#FFFFFF) @(1.0,1.0)

## Dropdown List

### Varient=Profile, State=Default
- Varient=Profile, State=Default | 195x243 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE) | 그림자 DROP(0,4,6,-2)#000000@0.05;DROP(0,10,15,-3)#000000@0.10
  - Profile | 195x83 | 가로 gap12 pad(20,20,20,20) 정렬 시작/끝 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
    - Frame 3916 | 155x43 | 세로 gap2 pad(0,0,0,0) 정렬 중앙/시작
      - Frame 1000007758 | 155x21 | 가로 gap10 pad(0,0,0,0) 정렬 양끝(SB)/중앙
        - Frame 1000007057 | 139x21 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
          - 담당자명 | 49x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '담당자명'
          - Badge | 40x17 | 가로 gap0 pad(8,0,8,0) 정렬 중앙/중앙 | 배경 Grey-100(#F5F6F7)
            - 관리자 | 29x17 | 색 Grey-400(#A4AAB0) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '관리자 '
        - 아이콘 Settings 16x16, stroke 1.8, 색 Grey-900(#000000)
      - email_adress@fursys.com | 155x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'email_adress@fursys.com'
  - Settings | 195x100 | 세로 gap20 pad(20,20,20,20) 정렬 시작/시작 | 배경 Grey-50(#FFFFFF)
    - Language | 155x60 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
      - Section | 155x18 | 세로 gap4 pad(0,0,0,0) 정렬 시작/시작
        - 언어 | 155x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '언어'
      - Select | 155x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
        - PlaceholderText | 115x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '한국어'
        - 아이콘 ChevronDown 16x16, stroke 1.0, 색 Grey-400(#A4AAB0)
  - Log Out | 195x60 | 가로 gap8 pad(20,20,20,20) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
    - 아이콘 LogOut 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
    - 로그아웃 | 46x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '로그아웃'

### Varient=Multiple, State=Hover
- Varient=Multiple, State=Hover | 220x256 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Input | 220x34 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
    - PlaceholderText | 180x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '검색'
    - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007702 | 220x222 | 세로 gap0 pad(4,4,4,4) 정렬 시작/시작
    - Input | 212x34 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x18 | 색 Grey-900(#000000) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '전체'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-100(#F5F6F7)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Hover
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'

### Varient=Multiple, State=Default
- Varient=Multiple, State=Default | 220x260 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Input | 220x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
    - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
    - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007702 | 220x224 | 세로 gap0 pad(4,4,4,4) 정렬 시작/시작
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '전체'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - Frame 1000007705 | 204x20 | 가로 gap8 pad(0,0,0,0) 정렬 중앙/중앙
        - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked
        - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'

### Varient=Single, State=Hover
- Varient=Single, State=Hover | 220x260 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Input | 220x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
    - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
    - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007702 | 220x224 | 세로 gap0 pad(4,4,4,4) 정렬 시작/시작
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '전체'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-100(#F5F6F7)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'

### Varient=Single, State=Default
- Varient=Single, State=Default | 220x260 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Input | 220x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
    - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
    - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007702 | 220x224 | 세로 gap0 pad(4,4,4,4) 정렬 시작/시작
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '전체'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'
    - Input | 212x36 | 가로 gap0 pad(8,8,8,8) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF)
      - PlaceholderText | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '드롭다운 텍스트'

## Table Cell

### Varient=Header, Type=Text
- Varient=Header, Type=Text | 52x32 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-100(#F5F6F7) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Frame 1000007707 | 20x17 | 가로 gap4 pad(0,0,0,0) 정렬 중앙/중앙
    - 번호 | 20x17 | 색 Gray/Gray-600(#B3B3B3) LIB! | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '번호'
  - Line 1 | 12x0 | 보더 Gray/Gray-400(#ECECEC) LIB! (전체 1px, CENTER)

### Varient=Header, Type=Radio
- Varient=Header, Type=Radio | 48x32 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-100(#F5F6F7) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Radio | 16x16 | 자유배치 | 인스턴스: State=Inactive

### Varient=Header, Type=Checkbox
- Varient=Header, Type=Checkbox | 48x32 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-100(#F5F6F7) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked

### Varient=Cell, Type=Calendar
- Varient=Cell, Type=Calendar | 128x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Input | 96x32 | 가로 gap12 pad(12,6,12,6) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'

### Varient=Cell, Type=Input
- Varient=Cell, Type=Input | 346x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Input | 314x32 | 가로 gap0 pad(12,6,12,6) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default

### Varient=Cell, Type=Icon
- Varient=Cell, Type=Icon | 48x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - 아이콘 Trash2 16x16, stroke 1.5, 색 Grey-300(#D6DADE)

### Varient=Cell, Type=Button
- Varient=Cell, Type=Button | 102x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Button | 70x24 | 가로 gap6 pad(10,2,10,2) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE) | 인스턴스: Varient=Secondary, Shape=Flat

### Varient=Cell, Type=Tag
- Varient=Cell, Type=Tag | 60x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Tag | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Red-100(#FFECEE) | 인스턴스: State=Light, Color=Red

### Varient=Cell, Type=Link
- Varient=Cell, Type=Link | 167x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - http://ap.fursys.com/... | 135x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'http://ap.fursys.com/...'

### Varient=Cell, Type=Textlink
- Varient=Cell, Type=Textlink | 66x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - 텍스트 | 34x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '텍스트'

### Varient=Cell, Type=Text
- Varient=Cell, Type=Text | 66x38 | 가로 gap4 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - 텍스트 | 34x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '텍스트'

### Varient=Cell, Type=Radio
- Varient=Cell, Type=Radio | 48x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Radio | 16x16 | 자유배치 | 인스턴스: State=Inactive

### Varient=Cell, Type=Checkbox
- Varient=Cell, Type=Checkbox | 48x38 | 가로 gap0 pad(16,0,16,0) 정렬 시작/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - Checkbox | 16x16 | 자유배치 | 인스턴스: State=Unchecked

## Search Filter

### State=Extended
- State=Extended | 1280x241 | 세로 gap8 pad(0,16,0,16) 정렬 끝/끝 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Frame 1000007021 | 1280x209 | 가로 gap16 pad(16,0,16,0) 정렬 시작/끝
    - Frame 1000007760 | 1070x209 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
      - Frame 1000007765 | 1070x59 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 314x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 고객사 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '고객사'
            - * | 285x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
        - Input Case | 348x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 314x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 기간 | 20x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '기간'
            - * | 294x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 348x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
            - Input | 136x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
            - Input | 208x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
              - 아이콘 Calendar 16x16, stroke 1.0, 색 Grey-400(#A4AAB0)
              - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
                - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
                - PlaceholderText | 6x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
                - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 품의 제목 | 42x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '품의 제목'
            - * | 124x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 작성자 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '작성자'
            - * | 137x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 상태 | 20x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '상태'
            - * | 146x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
      - Frame 1000007766 | 1070x59 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
      - Frame 1000007767 | 1070x59 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 165x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 165x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 분류명 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '분류명'
            - * | 136x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 165x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
    - Frame 1000007015 | 162x32 | 가로 gap4 pad(0,0,0,0) 정렬 끝/중앙
      - Button | 87x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999
        - 아이콘 Minus 12x12, stroke 2.0, 색 Grey-900(#000000)
        - 버튼명 | 45x18 | 색 Grey-900(#000000) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '상세 조회'
      - Button | 71x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE) | 인스턴스: Varient=Secondary, Shape=Round
  - Frame 1000007062 | 24x24 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
    - 아이콘 ChevronUp 16x16, stroke 1.8, 색 Grey-900(#000000)

### State=Default
- State=Default | 1280x91 | 세로 gap8 pad(0,16,0,16) 정렬 끝/끝 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - Frame 1000007021 | 1280x59 | 가로 gap16 pad(16,0,16,0) 정렬 시작/끝
    - Frame 1000007761 | 1070x59 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
      - Frame 1000007761 | 1070x59 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 314x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 고객사 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '고객사'
            - * | 285x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
        - Input Case | 348x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 314x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 기간 | 20x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '기간'
            - * | 294x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 348x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
            - Input | 136x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
            - Input | 208x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
              - 아이콘 Calendar 16x16, stroke 1.0, 색 Grey-400(#A4AAB0)
              - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
                - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
                - PlaceholderText | 6x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
                - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 품의 제목 | 42x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '품의 제목'
            - * | 124x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 작성자 | 29x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '작성자'
            - * | 137x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
        - Input Case | 166x59 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
          - Frame 1000007711 | 166x17 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
            - 상태 | 20x17 | 색 Grey-500(#7C8084) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '상태'
            - * | 146x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '*'
          - Input | 166x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
    - Frame 1000007015 | 162x32 | 가로 gap4 pad(0,0,0,0) 정렬 끝/중앙
      - Button | 87x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 인스턴스: Varient=Primary, Shape=Text
      - Button | 71x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE) | 인스턴스: Varient=Secondary, Shape=Round
  - Frame 1000007020 | 24x24 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
    - 아이콘 ChevronUp 16x16, stroke 1.8, 색 Grey-900(#000000)

## Input Case

### Varient=Text
- Varient=Text | 124x44 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
  - 서브 타이틀 | 56x18 | 색 Grey-500(#7C8084) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '서브 타이틀'
  - 텍스트를 입력해 주세요. | 124x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '텍스트를 입력해 주세요.'

### Varient=Field
- Varient=Field | 314x84 | 세로 gap6 pad(0,0,0,0) 정렬 시작/시작
  - Frame 1000007711 | 314x18 | 가로 gap0 pad(0,0,0,0) 정렬 중앙/중앙
    - 서브 타이틀 | 56x18 | 색 Grey-500(#7C8084) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '서브 타이틀'
    - * | 258x18 | 색 Red-600(#FF3A4A) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '*'
  - Input | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Text, State=Default
  - Frame 1000007060 | 314x18 | 가로 gap4 pad(0,0,0,0) 정렬 시작/중앙
    - 아이콘 CircleAlert 16x16, stroke 1.5, 색 System/Red/Red-200(#EF2E32) LIB! [숨김]
    - 에러 메세지 | 56x18 | 색 Red-600(#FF3A4A) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '에러 메세지'

## Input

### Varient=Date, State=Disabled
- Varient=Date, State=Disabled | 218x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - 아이콘 Calendar 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
    - PlaceholderText | 6x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'

### Varient=Date, State=Filled
- Varient=Date, State=Filled | 218x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - 아이콘 Calendar 16x16, stroke 1.2, 색 Grey-900(#000000)
  - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
    - PlaceholderText | 72x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
    - PlaceholderText | 6x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
    - PlaceholderText | 72x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'

### Varient=Date, State=Hover
- Varient=Date, State=Hover | 218x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - 아이콘 Calendar 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
    - PlaceholderText | 6x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'

### Varient=Date, State=Default
- Varient=Date, State=Default | 218x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - 아이콘 Calendar 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
  - Frame 1000007058 | 166x20 | 가로 gap8 pad(0,0,0,0) 정렬 시작/중앙
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'
    - PlaceholderText | 6x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '-'
    - PlaceholderText | 72x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '0000/00/00'

### Varient=Stepper, State=Disabled
- Varient=Stepper, State=Disabled | 82x34 | 가로 gap0 pad(12,0,0,0) 정렬 시작/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - Frame 1000007059 | 50x34 | 가로 gap10 pad(0,0,0,0) 정렬 중앙/중앙
    - PlaceholderText | 50x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '0'
  - Frame 2285 [숨김] | 20x34 | 세로 gap2 pad(0,0,0,0) 정렬 중앙/중앙 | 보더 Gray/Gray-400(#ECECEC) LIB! (좌 1px, INSIDE)
    - 아이콘 ChevronUp 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!
    - Vector 3 | 0x20 | 보더 Gray/Gray-400(#ECECEC) LIB! (전체 1px, CENTER)
    - 아이콘 ChevronDown 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!

### Varient=Stepper, State=Filled
- Varient=Stepper, State=Filled | 82x34 | 가로 gap0 pad(12,0,0,0) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - Frame 1000007059 | 50x34 | 가로 gap10 pad(0,0,0,0) 정렬 중앙/중앙
    - PlaceholderText | 50x18 | 색 Grey-900(#000000) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '0'
  - Frame 2285 [숨김] | 20x34 | 세로 gap2 pad(0,0,0,0) 정렬 중앙/중앙 | 보더 Gray/Gray-400(#ECECEC) LIB! (좌 1px, INSIDE)
    - 아이콘 ChevronUp 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!
    - Vector 3 | 0x20 | 보더 Gray/Gray-400(#ECECEC) LIB! (전체 1px, CENTER)
    - 아이콘 ChevronDown 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!

### Varient=Stepper, State=Hover
- Varient=Stepper, State=Hover | 82x34 | 가로 gap0 pad(12,0,0,0) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - Frame 1000007059 | 50x34 | 가로 gap10 pad(0,0,0,0) 정렬 중앙/중앙
    - PlaceholderText | 50x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '0'
  - Frame 2285 | 20x34 | 세로 gap2 pad(0,0,0,0) 정렬 중앙/중앙 | 보더 Grey-200(#EAEDF0) (좌 1px, INSIDE)
    - 아이콘 ChevronUp 12x12, stroke 1.6, 색 Grey-400(#A4AAB0)
    - Vector 3 | 0x20 | 보더 Grey-200(#EAEDF0) (전체 1px, CENTER)
    - 아이콘 ChevronDown 12x12, stroke 1.6, 색 Grey-400(#A4AAB0)

### Varient=Stepper, State=Default
- Varient=Stepper, State=Default | 82x34 | 가로 gap0 pad(12,0,0,0) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - Frame 1000007059 | 50x34 | 가로 gap10 pad(0,0,0,0) 정렬 중앙/중앙
    - PlaceholderText | 50x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body4-Regular (Regular 12) | 내용 '0'
  - Frame 2285 [숨김] | 20x34 | 세로 gap2 pad(0,0,0,0) 정렬 중앙/중앙 | 보더 Gray/Gray-400(#ECECEC) LIB! (좌 1px, INSIDE)
    - 아이콘 ChevronUp 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!
    - Vector 3 | 0x20 | 보더 Gray/Gray-400(#ECECEC) LIB! (전체 1px, CENTER)
    - 아이콘 ChevronDown 12x12, stroke 1.6, 색 Gray/Gray-600(#B3B3B3) LIB!

### Varient=Search, State=Disabled
- Varient=Search, State=Disabled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
  - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)

### Varient=Search, State=Filled
- Varient=Search, State=Filled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
  - 아이콘 Search 16x16, stroke 1.2, 색 Grey-900(#000000)

### Varient=Search, State=Hover
- Varient=Search, State=Hover | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
  - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)

### Varient=Search, State=Default
- Varient=Search, State=Default | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '검색'
  - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)

### Varient=Unit, State=Disabled
- Varient=Unit, State=Disabled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 268x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '9,999'
  - PlaceholderText | 22x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'mm'

### Varient=Unit, State=Filled
- Varient=Unit, State=Filled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 268x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '9,999'
  - PlaceholderText | 22x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'mm'

### Varient=Unit, State=Hover
- Varient=Unit, State=Hover | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 268x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '숫자 입력'
  - PlaceholderText | 22x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'mm'

### Varient=Unit, State=Default
- Varient=Unit, State=Default | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 268x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '숫자 입력'
  - PlaceholderText | 22x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 'mm'

### Varient=Dropdown, State=Disabled
- Varient=Dropdown, State=Disabled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 290x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '선택 완료'
  - 아이콘 ChevronDown 16x16, stroke 1.2, 색 Gray/Gray-600(#B3B3B3) LIB! [숨김]

### Varient=Dropdown, State=Filled
- Varient=Dropdown, State=Filled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '선택 완료'
  - 아이콘 ChevronDown 16x16, stroke 1.2, 색 Grey-900(#000000)

### Varient=Dropdown, State=Hover
- Varient=Dropdown, State=Hover | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '옵션 선택'
  - 아이콘 ChevronDown 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)

### Varient=Dropdown, State=Default
- Varient=Dropdown, State=Default | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 274x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '옵션 선택'
  - 아이콘 ChevronDown 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)

### Varient=Composite, State=Disabled
- Varient=Composite, State=Disabled | 337x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
  - Input | 120x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
  - Input | 213x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Date, State=Default

### Varient=Composite, State=Filled
- Varient=Composite, State=Filled | 337x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
  - Input | 120x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
  - Input | 213x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Date, State=Default

### Varient=Composite, State=Hover
- Varient=Composite, State=Hover | 337x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
  - Input | 120x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
  - Input | 213x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Date, State=Default

### Varient=Composite, State=Default
- Varient=Composite, State=Default | 337x36 | 가로 gap4 pad(0,0,0,0) 정렬 시작/끝
  - Input | 120x36 | 가로 gap0 pad(12,8,12,8) 정렬 양끝(SB)/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Dropdown, State=Default
  - Input | 213x36 | 가로 gap12 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE) | 인스턴스: Varient=Date, State=Default

### Varient=Text, State=Disabled
- Varient=Text, State=Disabled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-200(#EAEDF0) | 보더 Grey-300(#D6DADE) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 290x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '입력 완료'

### Varient=Text, State=Filled
- Varient=Text, State=Filled | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 290x20 | 색 Grey-900(#000000) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '입력 완료'

### Varient=Text, State=Hover
- Varient=Text, State=Hover | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-900(#000000) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 290x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '텍스트를 입력해 주세요.'

### Varient=Text, State=Default
- Varient=Text, State=Default | 314x36 | 가로 gap0 pad(12,8,12,8) 정렬 시작/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - PlaceholderText | 290x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body2-Regular (Regular 13) | 내용 '텍스트를 입력해 주세요.'

## Button

### Varient=Error, Shape=Square
- Varient=Error, Shape=Square | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Red-600(#FF3A4A) (전체 1px, CENTER)
  - 아이콘 Search 16x16, stroke 1.8, 색 Red-600(#FF3A4A)
  - 버튼명 | 34x20 | 색 Red-600(#FF3A4A) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Disabled, Shape=Flat
- Varient=Disabled, Shape=Flat | 70x24 | 가로 gap6 pad(10,0,10,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-200(#EAEDF0)
  - 아이콘 Plus 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 버튼명 | 32x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '버튼명'

### Varient=Secondary, Shape=Flat
- Varient=Secondary, Shape=Flat | 70x24 | 가로 gap6 pad(10,2,10,2) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - 아이콘 Plus 12x12, stroke 2.0, 색 Grey-900(#000000)
  - 버튼명 | 32x18 | 색 Grey-900(#000000) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '버튼명'

### Varient=Primary, Shape=Flat
- Varient=Primary, Shape=Flat | 70x24 | 가로 gap6 pad(10,0,10,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-900(#000000)
  - 아이콘 Plus 12x12, stroke 2.0, 색 Grey-50(#FFFFFF)
  - 버튼명 | 32x18 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '버튼명'

### Varient=Secondary, Shape=Text
- Varient=Secondary, Shape=Text | 74x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999
  - 아이콘 Plus 12x12, stroke 2.0, 색 Grey-400(#A4AAB0)
  - 버튼명 | 32x18 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '버튼명'

### Varient=Primary, Shape=Text
- Varient=Primary, Shape=Text | 74x32 | 가로 gap6 pad(12,0,12,0) 정렬 중앙/중앙 | r9999
  - 아이콘 Plus 12x12, stroke 2.0, 색 Grey-900(#000000)
  - 버튼명 | 32x18 | 색 Grey-900(#000000) | 텍스트 Body/Body3-SemiBold (SemiBold 12) | 내용 '버튼명'

### Varient=Disabled, Shape=Round
- Varient=Disabled, Shape=Round | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-200(#EAEDF0)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-400(#A4AAB0)
  - 버튼명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Secondary, Shape=Round
- Varient=Secondary, Shape=Round | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-900(#000000)
  - 버튼명 | 34x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Primary, Shape=Round
- Varient=Primary, Shape=Round | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r9999 | 배경 Grey-900(#000000)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-50(#FFFFFF)
  - 버튼명 | 34x20 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Disabled, Shape=Square
- Varient=Disabled, Shape=Square | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r4 | 배경 Grey-200(#EAEDF0)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-400(#A4AAB0)
  - 버튼명 | 34x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Secondary, Shape=Square
- Varient=Secondary, Shape=Square | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-900(#000000)
  - 버튼명 | 34x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

### Varient=Primary, Shape=Square
- Varient=Primary, Shape=Square | 82x32 | 가로 gap8 pad(12,0,12,0) 정렬 중앙/중앙 | r4 | 배경 Grey-900(#000000)
  - 아이콘 Search 16x16, stroke 1.8, 색 Grey-50(#FFFFFF)
  - 버튼명 | 34x20 | 색 Grey-50(#FFFFFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '버튼명'

## Tag

### State=Dark, Color=Black
- State=Dark, Color=Black | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Grey-900(#000000)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Black
- State=Light, Color=Black | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
  - 태그 | 20x17 | 색 Grey-900(#000000) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Dark, Color=Gray
- State=Dark, Color=Gray | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Grey-400(#A4AAB0)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Gray
- State=Light, Color=Gray | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Grey-100(#F5F6F7)
  - 태그 | 20x17 | 색 Grey-400(#A4AAB0) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Dark, Color=Blue
- State=Dark, Color=Blue | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Blue-500(#357FFF)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Blue
- State=Light, Color=Blue | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Blue-100(#E3EDFF)
  - 태그 | 20x17 | 색 Blue-500(#357FFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Dark, Color=Green
- State=Dark, Color=Green | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 TagGreen(#38BA77)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Green
- State=Light, Color=Green | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 TagGreenBG(#E7F6E7)
  - 태그 | 20x17 | 색 TagGreen(#38BA77) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Dark, Color=Yellow
- State=Dark, Color=Yellow | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 TagYellow(#E8C32E)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Yellow
- State=Light, Color=Yellow | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 TagYellowBG(#FCF7DF)
  - 태그 | 20x17 | 색 TagYellow(#E8C32E) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Dark, Color=Red
- State=Dark, Color=Red | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Red-600(#FF3A4A)
  - 태그 | 20x17 | 색 Grey-50(#FFFFFF) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

### State=Light, Color=Red
- State=Light, Color=Red | 28x16 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r2 | 배경 Red-100(#FFECEE)
  - 태그 | 20x17 | 색 Red-600(#FF3A4A) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '태그'

## Side Bar

### Varient=Favorite, States=Default
- Varient=Favorite, States=Default | 256x1080 | 세로 gap24 pad(12,0,12,0) 정렬 시작/시작 | 배경 Grey-50(#FFFFFF) | 보더 Gray/Gray-400(#ECECEC) LIB! (우 1px, OUTSIDE)
  - Frame 1000007000 | 232x107.294 | 세로 gap20 pad(0,24,0,0) 정렬 시작/시작
    - Frame 1000007777 | 94x25.2939 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
      - Attention | 18x25.2939 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden) | 인스턴스: Sort=Attention, Color=Black
      - (시스템명) | 60x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '(시스템명)'
    - Search | 232x38 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
      - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
      - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '검색'
  - Frame 1000007001 | 232x312 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
    - Tab | 232x40 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작
      - Menu | 232x40 | 가로 gap0 pad(4,4,4,4) 정렬 시작/중앙 | r6 | 배경 Grey-100(#F5F6F7)
        - Default | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2
          - Tabs Text | 49x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '전체 메뉴'
        - Select | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 그림자 DROP(0,1,2,0)#000000@0.05
          - Tabs Text | 46x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '즐겨찾기'
    - List | 232x256 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Volume2 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '공지 사항'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Settings 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 시스템 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '시스템 관리'
      - Sidebar / SidebarMenuItem | 232x72 | 세로 gap0 pad(0,0,0,0) 정렬 시작/중앙
        - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
          - 아이콘 FolderSearch 16x16, stroke 1.2, 색 Grey-900(#000000)
          - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '기준 관리'
        - Frame 1000006997 | 232x38 | 가로 gap0 pad(20,0,20,0) 정렬 시작/중앙
          - Frame 1000006996 | 192x38 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '품목 관리'
            - Border | 0x38 | 보더 Grey-200(#EAEDF0) (전체 1px, CENTER)
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 BarChartBig 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 실적 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '실적 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Calculator 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 정산 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '정산 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardList 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 관리'

### Varient=Default, States=Extended
- Varient=Default, States=Extended | 256x1080 | 세로 gap24 pad(12,0,12,0) 정렬 시작/시작 | 배경 Grey-50(#FFFFFF) | 보더 Gray/Gray-400(#ECECEC) LIB! (우 1px, OUTSIDE)
  - Frame 1000007000 | 232x107.294 | 세로 gap20 pad(0,24,0,0) 정렬 시작/시작
    - Frame 1000007777 | 94x25.2939 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
      - Attention | 18x25.2939 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden) | 인스턴스: Sort=Attention, Color=Black
      - (시스템명) | 60x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '(시스템명)'
    - Search | 232x38 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
      - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
      - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '검색'
  - Frame 1000006998 | 232x852 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
    - Tab | 232x40 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작
      - Menu | 232x40 | 가로 gap0 pad(4,4,4,4) 정렬 시작/중앙 | r6 | 배경 Grey-100(#F5F6F7)
        - Select | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 그림자 DROP(0,1,2,0)#000000@0.05
          - Tabs Text | 49x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '전체 메뉴'
        - Default | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2
          - Tabs Text | 46x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '즐겨찾기'
    - List | 232x796 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 LayoutDashboard 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '대시 보드'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Volume2 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '공지 사항'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Settings 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '시스템 관리'
      - Sidebar / SidebarMenuItem | 232x396 | 세로 gap0 pad(0,0,0,0) 정렬 시작/중앙
        - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 인스턴스: Type=Collapsible, State=Default, Collapsed=False
        - Frame 1000006997 | 232x362 | 가로 gap0 pad(20,0,20,0) 정렬 시작/중앙
          - Frame 1000006996 | 192x362 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '품목 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '용역료 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '행사 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '온라인 품목 결재 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '온라인 품목 조회'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,8,20,8) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '쇼핑몰 품목 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '유통채널 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '쇼핑몰 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '배송사 관리'
            - Sidebar / SidebarMenuSubItem | 192x34 | 가로 gap12 pad(20,0,20,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
              - Sub Menu Item | 152x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '만족도 조사 관리'
            - Border | 0x386 | 보더 Grey-200(#EAEDF0) (전체 1px, CENTER)
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ScrollText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 계약 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '계약 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 BarChartBig 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 실적 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '실적 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Calculator 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 정산 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '정산 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Layers3 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 파렛트 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '파렛트 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Package 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 재고 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '재고 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 MessageSquareText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 고객 문의 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '고객 문의 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardPen 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 변경 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 변경 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardList 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 관리'

### Varient=Default, States=Hover
- Varient=Default, States=Hover | 256x1080 | 세로 gap24 pad(12,0,12,0) 정렬 시작/시작 | 배경 Grey-50(#FFFFFF) | 보더 Gray/Gray-400(#ECECEC) LIB! (우 1px, OUTSIDE)
  - Frame 1000007000 | 232x107.294 | 세로 gap20 pad(0,24,0,0) 정렬 시작/시작
    - Frame 1000007777 | 94x25.2939 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
      - Attention | 18x25.2939 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden) | 인스턴스: Sort=Attention, Color=Black
      - (시스템명) | 60x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '(시스템명)'
    - Search | 232x38 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
      - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
      - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '검색'
  - Frame 1000006998 | 232x490 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
    - Tab | 232x40 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작
      - Menu | 232x40 | 가로 gap0 pad(4,4,4,4) 정렬 시작/중앙 | r6 | 배경 Grey-100(#F5F6F7)
        - Select | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 그림자 DROP(0,1,2,0)#000000@0.05
          - Tabs Text | 49x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '전체 메뉴'
        - Default | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2
          - Tabs Text | 46x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '즐겨찾기'
    - List | 232x434 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Blue-100(#E3EDFF)
        - 아이콘 LayoutDashboard 16x16, stroke 1.2, 색 Blue-700(#003EFF)
        - Menu Item | 180x20 | 색 Blue-700(#003EFF) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '대시 보드'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Volume2 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '공지 사항'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Settings 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '시스템 관리'
      - Sidebar / SidebarMenuItem | 232x34 | 세로 gap0 pad(0,0,0,0) 정렬 시작/중앙
        - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 인스턴스: Type=Collapsible, State=Default, Collapsed=False
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ScrollText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 계약 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '계약 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 BarChartBig 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 실적 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '실적 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Calculator 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 정산 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '정산 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Layers3 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 파렛트 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '파렛트 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Package 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 재고 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '재고 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 MessageSquareText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 고객 문의 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '고객 문의 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardPen 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 변경 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 변경 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardList 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 관리'

### Varient=Default, States=Default
- Varient=Default, States=Default | 256x1080 | 세로 gap24 pad(12,0,12,0) 정렬 시작/시작 | 배경 Grey-50(#FFFFFF) | 보더 Gray/Gray-400(#ECECEC) LIB! (우 1px, OUTSIDE)
  - Frame 1000007000 | 232x107.294 | 세로 gap20 pad(0,24,0,0) 정렬 시작/시작
    - Frame 1000007777 | 94x25.2939 | 가로 gap16 pad(0,0,0,0) 정렬 시작/중앙
      - Attention | 18x25.2939 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden) | 인스턴스: Sort=Attention, Color=Black
      - (시스템명) | 60x21 | 색 Grey-900(#000000) | 텍스트 Title/Title5-SemiBold (SemiBold 14) | 내용 '(시스템명)'
    - Search | 232x38 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (상+우+하+좌 1px, INSIDE)
      - 아이콘 Search 16x16, stroke 1.2, 색 Grey-400(#A4AAB0)
      - PlaceholderText | 180x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '검색'
  - Frame 1000006998 | 232x490 | 세로 gap16 pad(0,0,0,0) 정렬 시작/시작
    - Tab | 232x40 | 세로 gap0 pad(0,0,0,0) 정렬 시작/시작
      - Menu | 232x40 | 가로 gap0 pad(4,4,4,4) 정렬 시작/중앙 | r6 | 배경 Grey-100(#F5F6F7)
        - Select | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r4 | 배경 Grey-50(#FFFFFF) | 그림자 DROP(0,1,2,0)#000000@0.05
          - Tabs Text | 49x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '전체 메뉴'
        - Default | 112x32 | 가로 gap8 pad(12,6,12,6) 정렬 중앙/중앙 | r2
          - Tabs Text | 46x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '즐겨찾기'
    - List | 232x434 | 세로 gap2 pad(0,2,0,2) 정렬 시작/시작
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 LayoutDashboard 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '대시 보드'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Volume2 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '공지 사항'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Settings 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '시스템 관리'
      - Sidebar / SidebarMenuItem | 232x34 | 세로 gap0 pad(0,0,0,0) 정렬 시작/중앙
        - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF) | 인스턴스: Type=Collapsible, State=Default, Collapsed=False
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ScrollText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 계약 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '계약 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 BarChartBig 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 실적 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '실적 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Calculator 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 정산 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '정산 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Layers3 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 파렛트 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '파렛트 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 Package 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 재고 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '재고 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 MessageSquareText 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 고객 문의 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '고객 문의 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardPen 16x16, stroke 1.2, 색 Grey-900(#000000)
        - 주문 변경 관리 | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 변경 관리'
      - Sidebar / SidebarMenuButton | 232x34 | 가로 gap12 pad(12,0,12,0) 정렬 시작/중앙 | r6 | 배경 Grey-50(#FFFFFF)
        - 아이콘 ClipboardList 16x16, stroke 1.2, 색 Grey-900(#000000)
        - Menu Item | 180x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '주문 관리'

## Header

### Header
- Header | 1344x50 | 가로 gap10 pad(24,0,24,0) 정렬 양끝(SB)/중앙 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (하 1px, INSIDE)
  - 아이콘 PanelLeft 20x20, stroke 1.44, 색 Grey-900(#000000)
  - Frame 1000006988 | 703x32 | 가로 gap24 pad(0,0,0,0) 정렬 끝/중앙
    - Frame 1000007706 | 20x20 | 자유배치
      - 아이콘 Bell 20x20, stroke 1.2, 색 Grey-900(#000000) @(0.0,0.0)
      - textBadge | 16x15 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | r9999 | 배경 Red-600(#FF3A4A) | 위치 (8.0,-6.0) | 인스턴스: Color=Error, Shape=Round, Size=S
    - Frame 1000007718 | 147x32 | 가로 gap4 pad(16,6,12,6) 정렬 중앙/중앙 | r9999 | 배경 Grey-50(#FFFFFF) | 보더 Grey-200(#EAEDF0) (전체 1px, INSIDE)
      - Frame 1000007734 | 99x20 | 가로 gap4 pad(0,0,0,0) 정렬 시작/중앙
        - Frame 1000007717 | 48x20 | 가로 gap2 pad(0,0,0,0) 정렬 시작/중앙
          - 담당자 | 34x20 | 색 Grey-900(#000000) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '담당자'
          - 님 | 12x20 | 색 Grey-400(#A4AAB0) | 텍스트 Body/Body1-SemiBold (SemiBold 13) | 내용 '님'
        - Badge | 47x17 | 가로 gap0 pad(4,0,4,0) 정렬 중앙/중앙 | 배경 Grey-100(#F5F6F7)
          - 포지션명 | 39x17 | 색 Grey-400(#A4AAB0) | 텍스트 Caption/Caption1-SemiBold (SemiBold 11) | 내용 '포지션명'
      - 아이콘 ChevronDown 16x16, stroke 1.5, 색 Grey-400(#A4AAB0)

## Logo

### Sort=Signature, Color=Black
- Sort=Signature, Color=Black | 200x59.2902 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden)
  - Vector | 42.0275x59.2864 | 배경 LogoBlack(#1D1D1B) | 위치 (0.0,0.0)
  - Vector | 10.5975x56.9686 | 배경 LogoBlack(#1D1D1B) | 위치 (53.1,1.2)
  - Vector | 10.5975x56.9686 | 배경 LogoBlack(#1D1D1B) | 위치 (134.3,1.2)
  - Vector | 45.1718x56.9686 | 배경 LogoBlack(#1D1D1B) | 위치 (154.8,1.2)
  - Vector | 45.2904x56.9686 | 배경 LogoBlack(#1D1D1B) | 위치 (77.9,1.2)

### Sort=Signature, Color=White
- Sort=Signature, Color=White | 200x59.2902 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden)
  - Vector | 42.0275x59.2864 | 배경 Grey-50(#FFFFFF) | 위치 (0.0,0.0)
  - Vector | 10.5975x56.9686 | 배경 Grey-50(#FFFFFF) | 위치 (53.1,1.2)
  - Vector | 10.5975x56.9686 | 배경 Grey-50(#FFFFFF) | 위치 (134.3,1.2)
  - Vector | 45.1718x56.9686 | 배경 Grey-50(#FFFFFF) | 위치 (154.8,1.2)
  - Vector | 45.2904x56.9686 | 배경 Grey-50(#FFFFFF) | 위치 (77.9,1.2)

### Sort=Attention, Color=Black
- Sort=Attention, Color=Black | 60x84.3129 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden)
  - Vector | 60x84.3129 | 배경 Grey-900(#000000) | 위치 (0.0,0.0)

### Sort=Attention, Color=White
- Sort=Attention, Color=White | 60x84.3129 | 자유배치 | 배경 Grey-50(#FFFFFF) (hidden)
  - Vector | 60x84.3129 | 배경 Grey-50(#FFFFFF) | 위치 (0.0,0.0)


## 아이콘 사용 전수표 (컴포넌트 / 아이콘 / 크기 / stroke / 색)

| 컴포넌트(변형) | 아이콘 | 크기 | stroke | 색 |
|---|---|---|---|---|
| Pagination/Pagination | ChevronLeft | 16x16 | 1.2 | Grey-900(#000000) |
| Pagination/Pagination | ChevronRight | 16x16 | 1.2 | Grey-900(#000000) |
| Carousel/Varient=Navigator | ChevronLeft | 16x16 | 1.8 | Grey-900(#000000) |
| Carousel/Varient=Navigator | ChevronRight | 16x16 | 1.8 | Grey-900(#000000) |
| Tab/Varient=Line | Sun | 16x16 | 1.33 | - |
| Toast Popup/State=Error | X | 12x12 | 2.4 | Grey-50(#FFFFFF) |
| Toast Popup/State=Default | Check | 12x12 | 2.4 | Grey-50(#FFFFFF) |
| Breadcrumb/Breadcrumb | ChevronRight | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Breadcrumb/Breadcrumb | ChevronRight | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Breadcrumb/Breadcrumb | ChevronRight | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Breadcrumb/Breadcrumb | ChevronRight | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Check Box/State=Disabled | Minus | 11x11 | 2.18 | Grey-50(#FFFFFF) |
| Check Box/State=Multiple Checked | Check | 11x11 | 2.18 | Grey-900(#000000) |
| Check Box/State=Checked | Check | 11x11 | 2.18 | Grey-50(#FFFFFF) |
| Dropdown List/Varient=Profile, State=Default | Settings | 16x16 | 1.8 | Grey-900(#000000) |
| Dropdown List/Varient=Profile, State=Default | ChevronDown | 16x16 | 1.0 | Grey-400(#A4AAB0) |
| Dropdown List/Varient=Profile, State=Default | LogOut | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Dropdown List/Varient=Multiple, State=Hover | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Dropdown List/Varient=Multiple, State=Default | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Dropdown List/Varient=Single, State=Hover | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Dropdown List/Varient=Single, State=Default | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Table Cell/Varient=Cell, Type=Icon | Trash2 | 16x16 | 1.5 | Grey-300(#D6DADE) |
| Search Filter/State=Extended | Calendar | 16x16 | 1.0 | Grey-400(#A4AAB0) |
| Search Filter/State=Extended | Minus | 12x12 | 2.0 | Grey-900(#000000) |
| Search Filter/State=Extended | ChevronUp | 16x16 | 1.8 | Grey-900(#000000) |
| Search Filter/State=Default | Calendar | 16x16 | 1.0 | Grey-400(#A4AAB0) |
| Search Filter/State=Default | ChevronUp | 16x16 | 1.8 | Grey-900(#000000) |
| Input Case/Varient=Field | CircleAlert | 16x16 | 1.5 | System/Red/Red-200(#EF2E32) LIB! |
| Input/Varient=Date, State=Disabled | Calendar | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Date, State=Filled | Calendar | 16x16 | 1.2 | Grey-900(#000000) |
| Input/Varient=Date, State=Hover | Calendar | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Date, State=Default | Calendar | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Stepper, State=Disabled | ChevronUp | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Stepper, State=Disabled | ChevronDown | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Stepper, State=Filled | ChevronUp | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Stepper, State=Filled | ChevronDown | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Stepper, State=Hover | ChevronUp | 12x12 | 1.6 | Grey-400(#A4AAB0) |
| Input/Varient=Stepper, State=Hover | ChevronDown | 12x12 | 1.6 | Grey-400(#A4AAB0) |
| Input/Varient=Stepper, State=Default | ChevronUp | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Stepper, State=Default | ChevronDown | 12x12 | 1.6 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Search, State=Disabled | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Search, State=Filled | Search | 16x16 | 1.2 | Grey-900(#000000) |
| Input/Varient=Search, State=Hover | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Search, State=Default | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Dropdown, State=Disabled | ChevronDown | 16x16 | 1.2 | Gray/Gray-600(#B3B3B3) LIB! |
| Input/Varient=Dropdown, State=Filled | ChevronDown | 16x16 | 1.2 | Grey-900(#000000) |
| Input/Varient=Dropdown, State=Hover | ChevronDown | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Input/Varient=Dropdown, State=Default | ChevronDown | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Button/Varient=Error, Shape=Square | Search | 16x16 | 1.8 | Red-600(#FF3A4A) |
| Button/Varient=Disabled, Shape=Flat | Plus | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Button/Varient=Secondary, Shape=Flat | Plus | 12x12 | 2.0 | Grey-900(#000000) |
| Button/Varient=Primary, Shape=Flat | Plus | 12x12 | 2.0 | Grey-50(#FFFFFF) |
| Button/Varient=Secondary, Shape=Text | Plus | 12x12 | 2.0 | Grey-400(#A4AAB0) |
| Button/Varient=Primary, Shape=Text | Plus | 12x12 | 2.0 | Grey-900(#000000) |
| Button/Varient=Disabled, Shape=Round | Search | 16x16 | 1.8 | Grey-400(#A4AAB0) |
| Button/Varient=Secondary, Shape=Round | Search | 16x16 | 1.8 | Grey-900(#000000) |
| Button/Varient=Primary, Shape=Round | Search | 16x16 | 1.8 | Grey-50(#FFFFFF) |
| Button/Varient=Disabled, Shape=Square | Search | 16x16 | 1.8 | Grey-400(#A4AAB0) |
| Button/Varient=Secondary, Shape=Square | Search | 16x16 | 1.8 | Grey-900(#000000) |
| Button/Varient=Primary, Shape=Square | Search | 16x16 | 1.8 | Grey-50(#FFFFFF) |
| Side Bar/Varient=Favorite, States=Default | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Side Bar/Varient=Favorite, States=Default | Volume2 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Favorite, States=Default | Settings | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Favorite, States=Default | FolderSearch | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Favorite, States=Default | BarChartBig | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Favorite, States=Default | Calculator | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Favorite, States=Default | ClipboardList | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Side Bar/Varient=Default, States=Extended | LayoutDashboard | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Volume2 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Settings | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | ScrollText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | BarChartBig | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Calculator | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Layers3 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | Package | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | MessageSquareText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | ClipboardPen | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Extended | ClipboardList | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Side Bar/Varient=Default, States=Hover | LayoutDashboard | 16x16 | 1.2 | Blue-700(#003EFF) |
| Side Bar/Varient=Default, States=Hover | Volume2 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | Settings | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | ScrollText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | BarChartBig | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | Calculator | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | Layers3 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | Package | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | MessageSquareText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | ClipboardPen | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Hover | ClipboardList | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Search | 16x16 | 1.2 | Grey-400(#A4AAB0) |
| Side Bar/Varient=Default, States=Default | LayoutDashboard | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Volume2 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Settings | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | ScrollText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | BarChartBig | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Calculator | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Layers3 | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | Package | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | MessageSquareText | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | ClipboardPen | 16x16 | 1.2 | Grey-900(#000000) |
| Side Bar/Varient=Default, States=Default | ClipboardList | 16x16 | 1.2 | Grey-900(#000000) |
| Header/Header | PanelLeft | 20x20 | 1.44 | Grey-900(#000000) |
| Header/Header | Bell | 20x20 | 1.2 | Grey-900(#000000) |
| Header/Header | ChevronDown | 16x16 | 1.5 | Grey-400(#A4AAB0) |