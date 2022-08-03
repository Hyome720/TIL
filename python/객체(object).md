# 객체 (Object)

## 객체 리터럴 (Object Literal)

- **이름-값 쌍 (name-value pair)** 속성 (property)으로 이루어진 자료 구조

```javascript
const person = {
    name: '아이유', // 속성 이름 - 'name', 속성 값 - '아이유'
    age: 29, // 속성 이름 - 'age', 속성 값 - 29
    'Languages': ['Korean', 'Japanese'], // 속성 이름 - 'Languages', 속성 값 - 배열
    '한국 나이': 30 // 속성 이름 - '한국 나이', 속성 값 - 30
};
```

- 이미 정의된 변수의 이름을 속성의 값으로 사용할 수도 있음
- 대괄호를 사용해 다른 변수에 지정된 문자열을 속성 이름으로 사용 가능

```javascript
const propName = 'prop';

const obj = {
    [propName]: 1
};

obj.prop; // 1
```



### 점 표기법, 대괄호 표기법

- **속성 접근자 (property accessor)**를 이용해 이미 생성된 객체의 속성 지정 가능

```javascript
const person = {}; // 빈 객체

// 점 표기법 (Dot notation)
person.name = '아이유';
person.age = 30;
person.languages= ['Korean', 'Japanese'];

// 대괄호 표기법 (Bracket notation)
// 식별자로 허용되지 않는 문자가 들어간 경우
person['한국 나이'] = 20;
```

![image-20220803225329420](객체(object).assets/image-20220803225329420.png)

※ 의문점 : 왜 이 예시에서 Languages는 ''로 문자열 취급을 해주었는가?



### 객체 다루기

```javascript
// 속성 읽기
객체 이름.속성 이름; // '속성 값'

// 속성 쓰기
객체 이름.속성 이름 = '속성 값';

// 속성 삭제하기
delete 객체 이름.속성 이름;

// 속성이 객체에 존재하는지 확인하기
'속성 이름' in 객체 이름; // true or false
```



## 메소드 (Method)

- 객체의 속성값으로 **함수**도 지정 가능
- 객체의 속성으로 접근해서 사용하는 함수

```javascript
const person = {
    greet: function() {
        return 'hello';
    }
};

// ---------------------------------- 동일한 함수

const person = {
    greet() {
        return 'hello';
    }
};

person.greet(); // 'hello';
```



### this

- 메소드 호출 시에 해당 메소드를 갖고 있는 객체에 접근하는 키워드



## 프로토타입 (Prototype)

- **각각 다른 속성**을 지닌 객체들이 **공통으로 사용하는 속성과 메소드**를 중복해서 저장하지 않고    **재사용**할 수 있게 해주는 기능
- Object.create 함수를 이용
- **프로토타입 상속 (prototype inheritance)**
  - 한 객체에서 다른 객체의 기능을 가져와 사용하는 것
- 프로토타입을 간접적으로 변경하는 것은 불가능

```javascript
const personPrototype = {
    introduce: function() {
        return `안녕하세요, 제 이름은 ${this.name}입니다.`;
    }
};

const person1 = Object.create(personPrototype); // 새 객체를 생성하고 프로토타입 지정
person1.name = '아이유';

const person2 = Object.create(personPrototype);
person2.name = '백예린';

person1.introduce(); // 안녕하세요. 제 이름은 아이유입니다.
person2.introduce(); // 안녕하세요. 제 이름은 백예린입니다.

person1.introduce === person2.introduce; // true
```



### 프로토타입 읽고 쓰기

- Object.getPrototypeOf
  - 객체의 프로토타입 읽어오기
- Object.setPrototypeOf
  - 이미 생성된 객체의 프로토타입 변경
  - 단, 작업이 굉장히 느리므로 사용을 피하는 것이 좋음

```javascript
const parent = {
    familyName = '김'
};
const child = Object.create(parent);

Object.getPrototypeOf(child) === parent; // true

const newParent = {
    familyName = '이'
};
Object.setPrototypeOf(child, newParent);
Object.setPrototypeOf(child) === parent; // false
```



### 프로토타입 체인 (Prototype Chain)

```javascript
const parent = {
    a: 1
};
const child = {
    b: 2
};
Object.setPrototypeof(child, parent);
console.log(child); // { 'b': 2 }

// child 객체에는 a 속성이 없으나 출력하면 결과 값 
console.log(child.a); // 1 
```

- 프로토타입 객체의 속성까지 확인
  - 프로토타입 객체도 객체
    - 프로토타입 객체의 프로토타입 객체도 존재 가능
      - 더 이상 남아있는 프로토타입이 없을 때까지 확인

- Object.prototype.isPrototypeOf
  - 어떤 객체가 다른 객체의 프로토타입 체인에 존재하는지 확인



### 속성 가리기 (Property Shadowing)

```javascript
const parent = {
    prop: 1
};

const child = {
    prop: 2
};

Object.setPrototypeOf(child, parent); // 'child'의 프로토타입을 'parent'로 재정의

child.prop; // 프로토타입 체인에서 가장 먼저 만나는 값
```



### 생성자 (constructor)

- Object.create
- new

``` javascript
const obj = new Object();

typeof Object; // 'function'
```

