# 알람 시계 문제 풀이

백준 2884 문제
(https://www.acmicpc.net/problem/2884)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_HTML-CSS-publishing/assets/110072947/4208fa1b-1e58-4bb6-b645-7e020635cba2"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_HTML-CSS-publishing/assets/110072947/cfe1ff86-f5a7-4ee9-9341-caa1a1da7bfe"/></a>

<br/>
<br/>

## 내가 쓴 코드 (X)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");
let line = input[0].split(" ");

let a = parseInt(line[0]);
let b = parseInt(line[1]);

if (b > 45) {
  console.log(a, b - 45);
} else if (b == 45) {
  console.log(a);
} else if (b < 45) {
  console.log(a - 1, 60 + b - 45);
}
```

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let hour = Number(input[0].split(" ")[0]);
let minute = Number(input[0].split(" ")[1]);

if (minute < 45) {
  hour -= 1;
  minute += 15;
  if (hour < 0) hour = 23;
} else minute -= 45;

console.log(hour + " " + minute);
```
