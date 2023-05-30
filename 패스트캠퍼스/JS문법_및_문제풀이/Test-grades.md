# 시험 성적 문제 풀이

백준 9498 문제
(https://www.acmicpc.net/problem/9498)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_HTML-CSS-publishing/assets/110072947/c140392e-d02d-4235-aea0-5754b91d6081"/></a>

<br/>
<br/>

## 내가 쓴 코드 (O)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let a = Number(input[0]);

if (90 <= a && a <= 100) {
  console.log("A");
} else if (80 <= a && a <= 89) {
  console.log("B");
} else if (70 <= a && a <= 79) {
  console.log("C");
} else if (60 <= a && a <= 69) {
  console.log("D");
} else {
  console.log("F");
}
```

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

data = Number(input[0]);

function check(a) {
  if (90 <= a && a <= 100) console.log("A");
  else if (80 <= a && a <= 89) console.log("B");
  else if (70 <= a && a <= 79) console.log("C");
  else if (60 <= a && a <= 69) console.log("D");
  else console.log("F");
}

check(data);
```
