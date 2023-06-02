# 최댓값 문제 풀이

백준 2562 문제
(https://www.acmicpc.net/problem/2562)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/473c5563-c094-4f83-af17-3b2a8a2e1c66"/></a>

<br/>
<br/>

## 내가 쓴 코드 (OX)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let arr = [];

for (let i = 0; i < 9; i++) {
  arr.push(Number(input[i]));
}

let maxValue = arr.reduce((a, b) => Math.max(a, b));
let maxIndex = arr.indexOf(maxValue);

console.log(maxValue + "\n" + maxIndex);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 첫번째 방식 : 최댓값과 인덱스를 초기화하고, 배열의 원소를 하나씩 확인하며 최댓값과 인덱스 정보를 업데이트한다.
- 두번째 방식 : 함수를(map(), Math.max() , indexOf()) 사용한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let maxValue = 0;
let index = 0;
for (let i = 0; i < 9; i++) {
  let data = Number(input[i]);
  if (maxValue < data) {
    maxValue = data;
    maxIndex = i + 1;
  }
}

console.log(maxValue + "\n" + maxIndex);
```

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let data = input[1].split(" ").map(Number);

let min = data.reduce((a, b) => Math.min(a, b));
let max = data.reduce((a, b) => Math.max(a, b));

console.log(min, max);
```
