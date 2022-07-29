# number 타입

```javascript
7; // 정수 리터럴
2.5; // 부동 소수점 리터럴
0b111; // 2진수 리터럴 (binary literal)
0o777; // 8진수 리터럴 (octal literal)
0xf5; // 16진수 리터럴 (hexademical literal)
10_000 // 숫자 구분 기호 (Numeric Separators)

// 표기가 달라도 값이 같으면 똑같은 값이다.

typeof 위의 예시 값; // 'number' 로 전부 동일
```



## 정수 or 실수?

```javascript
Number.isInteger(1); // True
Number.isInteger(0.1); // false
```



## 다양한 연산

```javascript
// 산술 연산 (arithmetic operators)
1 + 2; // 더하기
3 - 4; // 빼기
5 * 6; // 곱하기
7 / 8; // 실수 나누기
9 % 10; // 나머지
11 ** 12; // 거듭제곱

// 비교 연산 (comparison operators)
1 < 2; // 작다
3 > 4; // 크다
5 <= 6; // 작거나 같다
6 >= 7; // 크거나 같다
8 === 8; // 같다
8 !== 9; // 같지 않다

// 증가/감소 연산 (increasement/decreasement operators)
let a = 1; ++a; // 연산결과 2, a === 2
let b = 1; b++; // 연산결과 1, b === 2
let c = 1; --c; // 연산결과 0, c === 0
let d = 1; d++; // 연산결과 1, d === 0

// 할당 연산 (assignment operators)
// x에 1을 더한 후 다시 x에 할당. x에는 1이 저장됨
let x = 0;
x += 1;

// `+=` 연산은 아래 연산과 같음
x = x + 1;

// 덧셈 뿐 아니라 다른 모든 산술 연산자도 할당 연산이 가능
x -= 1;
x *= 2;
x /= 3;
x %= 4;
x **= 5;
```



## 연산자 우선순위 (Operator Precedence)

- 기본적으로 연산자의 우선 순위를 따름
- 보통은 좌결합성 (좌측부터 계산)
- ** (제곱) 연산자는 우결합성 (우측부터 계산)



## 특이한 값들

- NaN
- -0
- Infinity
- -Infinity



## parseInt, parseFloat

- 문자를 number 타입으로 변경해주는 함수



## Math 객체

```javascript
// 상수
Math.E // 자연상수 (2.71...)
Math.PI // 원주율 (3.141592...)

// 삼각함수, 로그함수, 지수함수
Math.sin // 사인
Math.cos // 코사인
Math.tan // 탄젠트
Math.log // 로그함수
Math.exp // 지수함수
Math.sqrt // 제곱근

// 기타 등등
Math.abs // 절댓값
Math.ceil // 올림
Math.floor // 내림
Math.round // 반올림
Math.trunc // 소수점 아래 잘라내기

// 최대값, 최소값
Math.max
Math.min

// 랜덤
Math.random
```



