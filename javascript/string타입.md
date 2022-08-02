# string 타입

- 문자열 리터럴

```javascript
'hello'
"hello"
`hello world` // template literal
```

- 문자열에 대해서도 여러가지 연산자를 사용할 수 있음



### 템플릿 리터럴 (Template Literal)

- 문자열 리터럴의 일종
- 추가적인 기능을 제공

```javascript
const name1 = 'Foo';
const name2 = 'Bar';
const sentence = `${name1} meets ${name2}!`;
console.log(sentence); // Foo meets Bar!

`hello
world
hello
javascript!
` // 줄바꿈 인식
```




## Escape Sequence

- 특수 문자 앞에 \를 넣어 문자 그대로 사용할 수 있음



## 속성 및 메소드

- [String - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/String#String_instances)

```javascript
// 문자열의 길이
'hello'.length; // 5

// 여러 문자열 연결
'hello'.concat('fun', 'javascript'); // 'hellofunjavascript'

// 특정 문자열을 반복하는 새 문자열 생성
'*'.repeat(3); // '***'

//특정 문자열이 포함되어 있는지 확인
'hello javascript'.includes('hello'); // true
'hello javascript'.startsWith('he'); // true
'hello javascript'.endswith('ript'); // true
'hello javascript'.indexOf('java'); //6

// 문자열의 특정 부분을 바꾼 새 문자열 생성
'hello javascript'.replace('java', 'type'); // 'hello typescript'

// 문자열의 일부를 잘라낸 새 문자열 생성
'hello'.slice(2, 4); // 'll'

// 좌우 공백문자를 제거한 새 문자열 생성
'    hello    '.trim(); // 'hello'
'    hello    '.trimLeft(); // 'hello    '
'    hello    '.trimRight(); // '    hello'

// 좌우 공백문자를 추가한 새 문자열 생성
'hello'.padStart(8); // 'hello'
'hello'.padEnd(8); // 'hello    '

// 문자열을 특정 문자를 기준으로 잘라 새 배열 생성
'hello!fun!javascript'.split('!'); // ['hello', 'fun', 'javascript']
'hello'.split(''); // ['h', 'e', 'l', 'l', 'o']

// 모든 문자를 소문자, 혹은 대문자로 변환한 새 문자열 생성
'Hello JavaScript'.toLowerCase(); // 'hello javascript'
'Hello JavaScript'.toUpperCase(); // 'HELLO JAVASCRIPT'
```

