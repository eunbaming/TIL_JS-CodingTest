# 주사위 세개 문제 풀이

백준 2480 문제
(https://www.acmicpc.net/problem/2480)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/a0cbe769-1bc9-4293-b874-b0de1c694979"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/3d8c5378-240c-4580-a7c3-aad51e1cb5cf"/></a>

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let [a, b, c] = input[0].split(" ").map(Number);

if (a == b && b == c) console.log(10000 + 1000 * a);
else if (a == b) console.log(1000 + 100 * a);
else if (a == c) console.log(1000 + 100 * a);
else if (b == c) console.log(1000 + 100 * b);
else console.log(Math.max(a, b, c) * 100);
```

<br/>
<br/>

## 알게 된 것

- Math.max() : 입력값으로 받은 0개 이상의 숫자 중 가장 큰 숫자를 반환한다.

출처 : https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/max
