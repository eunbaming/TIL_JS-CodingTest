# 문자열 반복 문제 풀이

백준 2675 문제
(https://www.acmicpc.net/problem/2675)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/5d4f9c58-d01d-47cc-8365-22407ae758fb"/></a>

<br/>
<br/>

## 내가 쓴 코드 (X)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let answer = [];
let result = "";

for (let i = 1; i < n; i++) {
  answer.push(input[i].split(" "));
  for (let x of answer[1]) {
    for (let j = 1; j <= answer[0]; j++) {
      result += x;
    }
  }
  console.log(result);
}
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 한 줄씩 읽어들이면서, 문자열 s에 포함된 문자를 r번 반복한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let testCase = Number(input[0]);

for (let i = 1; i <= testCase; i++) {
  let [r, s] = input[i].split(" ");
  let result = "";

  for (let j = 0; j < s.length; j++) {
    result += s.charAt(j).repeat(r);
  }
  console.log(result);
}
```
