# ES6

ES6 모듈 시스템

```javascript
// a.js
export default function func1() {}  
// 내보낼경우 export 키워드 사용, defatult 키워드는 한 파일에 한번만 사
export function func2() {}
export const a1 = 123;
export let a2 = 'hello';

 // b.js
 import myFunc1, {func2, a1, a2} from './a.js'; 
 // 사용할경우 import, from 키워드 사
 // func1을 myFunc1이라는 이름으로 받아왔다. 
 // default 키워드 없이 내보내진 코드는 괋호를 사용하여 가져
 
 // c.js
 import { func2 as myFunc2 } from 'a.js'; 
 //as 키워드를 사용하여 이름 변경 가
```

