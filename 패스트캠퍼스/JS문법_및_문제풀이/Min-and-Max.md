# 최소, 최대 문제 풀이

백준 10818 문제
(https://www.acmicpc.net/problem/10818)

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

let n = Number(input[0]);
let arr = input[1].split(" ").map(Number); // 처음에 알지 못했던 부분

arr.sort((a, b) => a - b);

let min = arr[0];
let max = arr[n - 1];

console.log(min, max);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 첫번째 방식 : 최솟값, 최댓값을 초기화하고, 배열의 원소를 하나씩 확인하며 최댓값과 최솟값 정보를 업데이트한다.
- 두번째 방식 : reduce를 사용한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let arr = input[1].split(" ").map(Number);

// 모든 정수는 -1,000,000보다 크거나 같고, 1,000,000보다 작거나 같은 정수이다.

let min = 1000001; // 일단 큰 수로 초기화
let max = -1000001; // 일단 작은 수로 초기화

for (let i = 0; i < arr.length; i++) {
  if (min > arr[i]) min = arr[i];
  if (max < arr[i]) max = arr[i];
}

console.log(min, max);
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
