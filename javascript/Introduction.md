# 간단한 소개

- 1995년 웹 브라우저 Netscape Navigator에 처음으로 탑재
- Java와는 전혀 다른 언어



## 언어와 구동 환경

- 다른 범용 프로그래밍 언어에 비해서는 적은 양의 기능을 포함
- 웹 브라우저
- 웹 서버 (Node js)
- 게임 엔진
- 포토샵



## 브라우저 간 호환성

- 어느 브라우저든 기능이 잘 작동하도록 해주는 것
- 브라우저 간 호환성 문제를 해결해주는 **라이브러리** 등장
- **ECMAScript** 표준을 따라 브라우저를 구현하기 시작
- 최신 버전의 JavaScript를 지원하지 않는 브라우저와 호환을 도와주는 도구
  - 트랜스파일러 (transpiler)
  - 폴리필 (polyfill)

### 트랜스 파일러 (Transpiler)

- Javascript의 문법을 똑같이 동작하는 이전 버전 JavaScript의 문법으로 바꾸어주는 도구
  - Babel
  - Typescript

### 폴리필 (Polyfill) / 심 (shim)

- JavaScript의 문법과 기능을 구형 환경에서도 동일하게 구현해 놓은 라이브러리