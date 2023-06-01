# 별 찍기 문제 풀이

백준 2438 문제
(https://www.acmicpc.net/problem/2438)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/ca4dead7-8cd3-4899-9ef8-375d15350811"/></a>

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 2중 반복 문법을 이용해서 해결할 수 있다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");
let n = Number(input[0]);

for (let i = 1; i <= n; i++) {
  // 행만큼 반복 - 선생님은  // let i = 0 ; i < n //
  for (let j = i; j <= i; j++) {
    // 현재 행만큼 별을 출력 - 선생님은  // let j = 0 ; j <= i //
    result += "*";
  }
  result += "\n";
}
console.log(result);
```
