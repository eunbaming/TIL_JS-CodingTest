# 합 문제 풀이

백준 8393 문제
(https://www.acmicpc.net/problem/8393)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/9a2f7375-eeb4-437b-b642-eb7cf3e1e6f5"/></a>

<br/>
<br/>

## 내가 쓴 코드 (O)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let num = Number(input[0]);
let result = 0;

for (let i = 1; i <= num; i++) {
  result += i;
}

console.log(result);
```

<br/>
<br/>

## 선생님 해설

- 문자열을 수로 변환할 때 parseInt에 비하여 Number의 속도가 더 빠르게 동작한다.

### 문제 해결 아이디어

- 첫번째 방식 : 단순히 1부터 10,000까지의 값을 차례대로 더한다. 이 경우 시간복잡도 O(N)이다.
- 두번째 방식 : 등차수열의 합 공식을 이용할 수 있다. 이 경우 시간복잡도 상수시간이다.
  <br/>
  등차수열의 제 1항부터 제 N항 까지의 합을 S<sub>N</sub>라고 하자.
  첫째항이 a, 마지막 항이 m일 때
  <br/>
  S<sub>N</sub> = N(a + m) / 2

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let summary = 0;

for (let i = 1; i <= n; i++) {
  summary += i;
}

console.log(summary);
```

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);

console.log((n * (1 + n)) / 2);
```
