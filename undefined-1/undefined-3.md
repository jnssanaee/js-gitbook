# 배열 내장함수

### map

map 메서드는 배열 내 각 요소를 순회하며, 주어진 함수에 대입한 결과를 새로운 배열로 반환 

```javascript
//구문
arr.map(callback(currentValue[, index[, array]])[, thisArg])

//예
const array = [1, 2, 3];
const squared = array.map(n => n * n);
console.log(squared); // [1, 4, 9]
```



### indexOf

indexOf 메서드는 배열에서 지정된 요소**\(숫자, 문자, 불리언\)를 찾을 수있는 인덱스를 반환**하고, 존재하지 않으면 -1을 반환

```javascript
//구문
arr.indexOf(searchElement[, fromIndex]) 

//예제
const arr = [1, 2, 6];
console.log(arr.indexOf(6)); // 2
console.log(arr.indexOf(6, -1)); // 2 ??
console.log(arr.indexOf(6, 1)); // 2 ??
```



### findIndex

findIndex 메서드는 배열에서 지정된 요소**\(객체, 배열\)를 찾을 수 있는 인덱스를 반환**하고, 존재하지 않으면 -1을 반환 

```javascript
//구문
arr.findIndex(callback[, thisArg])

//예제
var arr = [
  {
    id: 1,
    name: 'korea'
  },
  {
    id: 2,
    name: 'japan'
  }
]
const index = arr.findIndex(todo => todo.id === 2);
console.log(index); // 1
```



### find

주어진 판별 함수를 만족하는 **첫번째 요소의 값 자체 반환**하고, 존재하지 않으 [`undefined`](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/undefined)를 반환

```javascript
//구문
arr.find(callback[, thisArg])

//예제
const arr = [5, 12, 8, 130, 44];
const found = array1.find(element => element > 10);
console.log(found); // 12
```



### filter

주어진 **함수를 만족하는 요소를 모아 새로운 배열로 반환** 

```javascript
const todos = [
  {
    id: 1,
    done: false
  },
  {
    id: 2,
    done: true
  },
  {
    id: 3,
    done: false
  }
];

const tasksNotDone = todos.filter(todo => todo.done === false);
console.log(tasksNotDone); //아래 배열 반환

[
  {
    id: 1,
    done: false
  },
  {
    id: 3,
    done: false
  }
];
```



### 





























