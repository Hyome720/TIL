# null과 undefined

- undefined
  - 값이 대입되지 않은 변수 혹은 속성을 사용하려고 할 때 반환

```javascript
let undf;
undf // undefined

const obj = {};
obj.prop; // undefined
```

- null
  - 객체가 없음

```javascript
typeof null // 'object'
```

- '없음'을 저장하는 법
  - null을 통해 명시적 부재를 나타내는 것이 좋음
  - 단, 객체에서 속성의 부재를 나타날 때는 그 속성을 정의하지 않는 것이 더 간편하여 널리 사용됨



## null check

```javascript
function printIfNotNull(input) {
    if (input !== null && input !== undefined) {
        console.log(input);
    }
}

// 아래 식으로도 사용 가능
// input !== null && input !== undefined;
// input != null;
// input != undefined;
-------------------------
// input === null || input === undefined;
// input == null;
// input == undefined;
```

- == 연산자
  - 한 쪽 피연산자에 null 혹은 undefined가 오면 다른 쪽 피연산자에 null 혹은 undefined가 왔을 때만 **true**를 반환하고, 다른 모든 경우에 **false** 반환