# JSX

- 자바스크립트의 확장 문법
  - XML과 유사



## 장점

- 보기 쉽고 익숙
  - HTML 코드를 작성하는 것과 유사
- 높은 활용도
  - HTML  태그 사용 가능
  - 컴포넌트도 작성 가능



## 문법

- 컴포넌트의 요소 여러개를 하나로 감싸주어야 함
- 컴포넌트 내부는 하나의 DOM 트리 구조로 이루어져야함
  - div 태그 또는 Fragment 또는 < > 사용 가능

```javascript
import React, { Fragement } form 'react';

function App() {
    return (
    	<Fragment>
            <h1>리액트 안녕~</h1>
            <h2>문제 없이 작동하니?</h2>
        </Fragment>
    );
}

export default App;
```

- 조건부 연산자
  - JSX 내에선 if 문이 사용 불가능하지만 { } 인안에 조건부 연산자(삼항 연산자) 사용 가능

```react
import React from 'react';

function App() {
    const name = '리액트';
    return (
    	<div>
        	{name === '리액트' ? (
            	<h1>리애특입니다.</h1>
            ) : (
            	<h2>리액트가 아닙니다.</h2>
            )}
        </div>
    );
}

export default App;

-------------------------------------------------------------------------------
    
import React from 'react';
 
function App() {
  const name = '뤼왝트';
  return <div>{name === '리액트' ? <h1>리액트입니다.</h1> : null}</div>;
}          {/* null 렌더링 시 아무것도 보여주지 않음 /}
 
export default App;


```

- **undefined**는 렌더링 시 오류 발생

- 인라인 스타일링
  - background-color  같이 - 문자가 포함되면 카멜표기법으로 작성
    - backgroundColor

```javascript
import React from ‘react‘;


function App() {
  const name = ‘리액트‘;
  const style = {
    // background-color는 backgroundColor와 같이 -가 사라지고 카멜 표기법으로 작성됩니다.
    backgroundColor: ‘black‘,
    color: ‘aqua‘,
    fontSize: ‘48px‘, // font-size -> fontSize
    fontWeight: ‘bold‘, // font-weight -> fontWeight
    padding: 16 // 단위를 생략하면 px로 지정됩니다.
  };
  return <div style={style}>{name} </div>;
}


export default App;
```

- class 이름 작성시 className으로 설정
  - App.css 파일에서 클래스를 작성
  - App.js의 div 요소에 className 지정

- HTML과 달리 input, br 등 닫는 태그가 필요
  - 내용이 없을 경우 **<input />**처럼도 작성 가능 



## css 적용

> 3가지 방법이 존재

1. Inline style로 작성
   - 잘 사용하지 않음

```
export default function <functionName>() {
	return (
		<div>
			<h1 style={
			{
				color: "red",
				backgroundColor: "blue",
				marginBottom: "30px",
				opacity: 0.5,
			}}
				Hello
			</h1>			
		</div>
	);
}
```

2. index.css / App.css 파일 활용
   - 요소 이름이 중복되어 에러가 발생할 수 있음

3. import styles from "./{파일명}.module.css" 파일 생성
   - className={styles.{클래스명}} 으로 작성
   - 동일한 클래스명이어도 다른 css 적용 가능
