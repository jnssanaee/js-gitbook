---
description: 작업을 수행하거나 값을 계산하는 문장 집합 같은 자바스크립트 절차
---

# 함수

### ES6 리터럴 

```javascript
// ES6의 템플릿 리터럴 문법으로 아래와 같이 사용 가능하다.
function hello(name) {
  console.log(`Hello, ${name}!`);
}
hello('velopert');
```

### 

### 화살표 함수

화살표 함수는 항상 익명이며, 자신의 this, arguments 등을 바인딩하지 않는다.  
메서드가 아닌 곳에 가장 적합하며, 생성자로서 사용할 수 없다. 

```javascript
const add = (a, b) => {
  return a + b;
};

//ES6 문법
const add = (a, b) => a + b;

// 객체 리터럴 반환 (객체 리터럴을 괄호로 감싸는 걸 기억하라!)
var func = () => {foo: 1}; // 호출 시 undefined 반환
var func = () => ({foo: 1}); // {foo: 1} 반환 
```



