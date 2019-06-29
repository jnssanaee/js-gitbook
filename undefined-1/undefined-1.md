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



### getter

getter는 어떤 프로퍼티에 접근할 때마다 그 값을 계산하도록 해야 하거나, 내부 변수의 상태를 명시적인 함수 호출 없이 보여주고 싶을 때 이용한다.

```javascript
const numbers = {
  a: 1,
  b: 2,
  get sum() {
    console.log('sum 함수가 실행');
    return this._a + this._b;
  }
};

// numbers.sum처럼 조회만 해도 함수가 실
console.log(numbers.sum); // 'sum 함수 실행', 3 (순차적으로 출력)
numbers.a = 5;
console.log(numbers.sum); // 'sum 함수 실행', 6 (순차적으로 출력)

delete numbers.sum // delete 연산자를 통해 getter를 삭제할 수 있다. 
```



### setter

setter는 어떤 객체의 속성에 이 속성을 설정하려고 할 때, 호출되는 함수를 바인드한다. 

```javascript
const numbers = {
  _a: 1,
  _b: 2,
  sum: 3,
  calculate() {
    console.log('calculate');
    this.sum = this._a + this._b;
  },
  get a() {
    return this._a;
  },
  set a(value) {
    console.log('a가 바뀝니다.');
    this._a = value;
    this.calculate();
  }
};
console.log(numbers.sum); // 3
numbers.a = 5; // 5가 파라미터로 들어감
console.log(numbers.sum); // 'a가 바뀝니다.', 'calculate', 7 (순차적으로 출력) 
```

