# 배열 내장함수

### map

map 메서드는 배열 내 각 요소를 순회하며, 주어진 함수에 대입한 결과를 새로운 배열로 반환 

```javascript
const array = [1, 2, 3];
const squared = array.map(n => n * n);
console.log(squared); // [1, 4, 9]
```

