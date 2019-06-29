# 반복문

### for .. in문

```javascript
const doggy = {
  name: '멍멍이',
  sound: '멍멍',
  age: 2
};

for (let key in doggy) {
  console.log(`${key}: ${doggy[key]}`);
}
// "name: 멍멍이"
// "sound: 멍멍"
// "age: 2"

// 비슷한 역할을 하는 Object 메서드가 있다.
console.log(Object.entries(doggy)); // [[키, 값], [키, 값]] 형태의 배열로 변환
console.log(Object.keys(doggy)); // [키, 키, 키] 형태의 배열로 변환
console.log(Object.values(doggy)); // [값, 값, 값] 형태의 배열로 변환
```

