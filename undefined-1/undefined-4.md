---
description: >-
  각각의 객체는 [[Prototype]]이라는 은닉 속성을 가지며, 이 속성은 자신의 프로토타입이 되는 객체를 가리킨다. null은 프로토타입
  체인의 종점 역할을 한다.
---

# 프로토타입과 클래스

### 생성

객체를 생성하는 함수를 **생성자 함수라고 부르며, new 키워드를 사용**해 생성한다. \(관행상 대문자로 시작한다.\) 

```javascript
function Animal(type, name, sound) {
  this.sound = sound;
  this.say = function() {
    console.log(this.sound);
  }
}

const dog = new Animal('개', '멍멍이', '멍멍');
dog.say(); // '멍멍'
```



### 프로토타입

같은 객체 생성자 함수를 사용하는 경우, 특정 함수 또는 값을 재사용 할 수 있는데 바로 프로토타입이다.  
프로토타입은 다음과 같이 객체 생성자 함수 아래에 `.prototype.[원하는키] =` 코드를 입력하여 설정 할 수 있다.

```javascript
function Animal(type, name, sound) {
  this.type = type;
  this.name = name;
  this.sound = sound;
}

Animal.prototype.say = function() {
  console.log(this.sound);
};
Animal.prototype.sharedValue = 1;

const dog = new Animal('개', '멍멍이', '멍멍');

dog.say(); // '멍멍'

console.log(dog.sharedValue); // 1
```



### 상속 \(다시 정리하자\)



### Class

es6에서 추가된 문법이며, 기존 prototype 기반의 상속보다 명료하게 사용할 수 있다. Class는 사실 **함수**다.































