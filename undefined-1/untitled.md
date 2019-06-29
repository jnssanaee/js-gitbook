---
description: '객체는 관련된 데이터와 함수(일반적으로 여러 데이터와 함수로 이루어지는데, 객체 안에 있을 때는 보통 프로퍼티와 메소드라고 부릅니다)의 집합'
---

# 객체

```javascript
// key에 공백이 있을 시 따옴표로 감싸줘야한다.
const sample = {
  'key with space': true
};
```

####  <a id="&#xD568;&#xC218;&#xC5D0;&#xC11C;-&#xAC1D;&#xCCB4;&#xB97C;-&#xD30C;&#xB77C;&#xBBF8;&#xD130;&#xB85C;-&#xBC1B;&#xAE30;"></a>

#### 함수에서 객체를 파라미터로 받기 <a id="&#xD568;&#xC218;&#xC5D0;&#xC11C;-&#xAC1D;&#xCCB4;&#xB97C;-&#xD30C;&#xB77C;&#xBBF8;&#xD130;&#xB85C;-&#xBC1B;&#xAE30;"></a>

```javascript
const ironMan = {
  name: '토니 스타크',
  actor: '로버트 다우니 주니어',
  alias: '아이언맨'
};

function print(hero) {
  const text = `${hero.alias} 역할을 맡은 배우는 ${hero.actor} 입니다.`;
  console.log(text);
}

print(ironMan); // '아이언맨 역할을 맡은 배우는 로버트 다우니 주니어 입니다.' 

// 아래와 같이 파라미터를 '객체 비구조화 할당'을 할 수도 있다. 
function print({ alias, name, actor }) {
  const text = `${alias}(${name}) 역할을 맡은 배우는 ${actor} 입니다.`;
  console.log(text);
}
```



