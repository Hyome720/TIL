# CSS

- Cascading Style Sheets
- 선택자 (Selector), 선언 (Declaration), 속성 (Property), 값 (Value) 로 구성
- 선택자를 통해 스타일을 지정할 HTML 요소 선택
- 중괄호 안에 속성과 값, 하나의 쌍으로 이루어진 선언 진행
- 속성 : 어떤 스타일 기능을 변경할 지 결정
- 값 : 어떻게 스타일 기능을 변경할 지 결정



## 정의 방법

- 인라인
  - 해당 태그에 직접 style 속성 활용
  - 실수가 잦아짐
    - 중복
    - 찾기 어려움
- 내부 참조
  - \<head> 태그 내에 \<style>에 지정
  - 코드가 길어짐
- 외부 참조
  - 외부 CSS 파일을 \<head> 내 \<link>를 통해 불러옴
  - 가장 널리 쓰임



## 선택자 (Selector)

- 기본 선택자
  - 전체 선택자
  - 요소 선택자
    - HTML 태그 직접 선택
  - 클래스 선택자
    - 마침표(.)로 시작
    - 해당 클래스가 적용된 항목 선택
  - 아이디 선택자
    - \# 로 시작
    - 해당 아이디가 적용된 항목 선택
    - 하나의 문서에 1번만 사용
    - 여러 번 사용해도 되나, 단일 id 사용 권장
  - 속성 선택자
- 결합자 (Combinators)
  - 자손 결합자 (공백)
    - selector A 하위의 모든 selector B 요소
  - 자식 결합자 (>)
    - selector A 바로 아래의 selector B 요소
  - 일반 형제 결합자 (~)
    - selector A의 형제 요소 중 뒤에 위치하는 selector B 요소 모두 선택
  -  인접 형제 결합자 (+)
    - selector A의 형제 요소 중 바로 뒤에 위치하는 selector B 요소 선택
- 의사 클래스/요소 (Pseudo Class)
  - 링크, 동적 의사 클래스
  - 구조적 의사 클래스, 기타 의사 클래스, 의사 요소, 속성 선택자

### 적용 우선순위 (cascading order)

1. 중요도 (Importance) - 사용시 주의
   - !important
2. 우선 순위 (Specificity)
   - 인라인 > id > class, 속성, pseudo-class > 요소, pseudo-element
3. CSS 파일 로딩 순서



## 기본 스타일

### 크기 단위

- px (픽셀)
  - 모니터 해상도의 화소
  - 고정적인 단위
- %
  - 백분율 단위
  - 가변적인 레이아웃에서 사용

- em
  - 상속을 받음 (바로 위의 부모 요소)
  - 배수 단위
  - 상대적인 사이즈
- rem 
  - 상속을 받지 않음
  - 최상위 요소(html)의 사이즈를 기준으로 배수 단위를 지님

- viewport
  - 디바이스의 viewport를 기준으로 상대적인 사이즈 결정
  - vw, vh, vmin, vmax

### 색상 단위

- 색상 키워드 (background-color: red)
  - 대소문자 구분 없음
  - 특정 색을 글자로 표현
- RGB 색상 (background-color: rgb(0, 255, 0);)
  - 16진수 혹은 함수형 표기법을 사용해 표현
- HSL 색상 (background-color: hsl(0, 100%, 50%);)
  - 색상, 채도, 명도를 통해 특정색을 표현



## Box model

- 모든 요소는 네모 (박스모델)
- 위에서 아래로 / 왼쪽에서 오른쪽으로 쌓임
- margin
  - 테두리 바깥의 외부 여백
  - 배경색 지정 불가
-  border
  - 테두리 영역
- padding
  - 테두리 안쪽의 내부 여백
  - 요소에 적용된 배경색
  - 이미지가 적용
- content
  - 글이나 이미지 등 요소의 실제 내용



## Display

- display: block
  - 줄 바꿈이 일어나는 요소
  - 화면 크기의 전체 가로 폭 차지
  - 인라인 레벨 요소가 들어갈 수 있음
  - div / ul, ol, li / p / hr / form
- display: inline
  - 줄 바꿈이 일어나지 않는 요소
  - content 너비만큼 가로 폭 차지
  - width, height, margin-top, margin-bottom 지정 불가
  - 상하 여백은 line-height로 지정
  - span / a / img / input, label / b, em, i, strong

- display: inline-block
  - block과 inline 레벨 요소의 특징을 가짐
  - inline 처럼 한줄에 표시 가능
  - block 처럼 width, height, margin 속성 지정 가능
- display: none
  - 해당 요소 화면에 표시 x
  - 공간 부여 x
  - visibility: hidden은 공간 부여



## Position

- static
  - 모든 태그의 기본 값 (기준 위치)
  - 일반적인 요소 배치 순서에 따름 (좌측 상단)
  - 부모 요소 내에선 부모 요소의 위치를 기준으로 배치
- relative
  - 상대 위치
  - 자기 자신의 static 위치를 기준으로 이동
- absolute 
  - 절대 위치
  - 가장 가까이 있는 부모/조상 요소를 기준으로 이동
- fixed
  - 고정 위치
  - 부모 요소과 관계 없이 viewport 기준으로 이동
  - 스크롤 시에도 같은 곳에 위치

- sticky
  - 스크롤에 따라 static => fixed로 변경