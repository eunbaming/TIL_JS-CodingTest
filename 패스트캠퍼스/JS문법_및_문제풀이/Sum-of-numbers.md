# 숫자의 합 문제 풀이

백준 11720 문제
(https://www.acmicpc.net/problem/11720)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/db122a68-a607-4d71-b4c5-05eb07f547fe"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/faf555a6-a3f8-4331-bed6-b945257a41c8"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/26af40a9-9a37-4d57-a34c-d5d212dd1060"/></a>

<br/>
<br/>

## 내가 쓴 코드 (O)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let num = Number(input[0]);
let data = input[1].split("").map(Number);
let result = 0;

for (let i = 0; i < num; i++) {
  result += data[i];
}

console.log(result);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- for~of문을 사용한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let string = input[1];
let answer = 0;

for (let x of string) {
  answer += Number(x);
}

console.log(answer);
```
