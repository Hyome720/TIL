# boolean 타입

- true
- false



## 논리 연산자

- ! : 논리 부정
- || : 논리 합 (or)
  - A || B
  - A가 falsy면 B 생성
- && : 논리 곱 (and)
  - A && B
  - A가 truthy면 B 생성
- ||= 
  - 변수의 값이 true일 경우 : 변화 x
  - 변수의 값이 false일 경우 : 우항의 값이 변수에 할당
- &&=
  - 변수의 값이 true일 경우 : 우항의 값이 변수에 할당
  - 변수의 값이 false일 경우 : 변화 x
- condition ? exprIfTrue : exprIfFalse
  - 3항 연산자
  - condition - 조건문
  - exprIfTrue - 조건문이 truthy 일 때 실행되는 표현식
  - exprIfFalse - 조건문이 falsy 일 때 실행되는 표현식



### truthy 와 falsy

- falsy
  - false
  - null
  - undefined
  - 0
  - NaN
  - ' '
- truthy
  - falsy를 제외한 값