# 오븐 시계 문제 풀이

백준 2525 문제
(https://www.acmicpc.net/problem/2525)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_HTML-CSS-publishing/assets/110072947/e21eb2b6-49ee-4a75-b7e0-0dc1d4fa04c7"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_HTML-CSS-publishing/assets/110072947/23b7b813-b0b1-46e4-a1ce-62e9c9242f75"/></a>

<br/>
<br/>

## 내가 쓴 코드 (X)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let hour = Number(input[0].split(" ")[0]);
let minute = Number(input[0].split(" ")[1]);
let time = Number(input[1]);

if (miute + time >= 60) {
  hour += 1;
  minute = time - (60 - minute);
  if (hour === 24) {
    hour = 0;
  }
} else {
  minute += time;
}
console.log(hour + " " + minute);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 입력으로 주어진 시각을 '분'의 형태로 바꾼다.
- '분'이 주어졌을 때, 시각을 알려주는 기능을 작성한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let [a, b] = input[0].split(" ").map(Number);
let c = Number(input[1]);

let totalMinute = a * 60 + b + c;
totalMinute %= 1440; // 하루가 넘어가지 않도록 해준다.
let hour = parseInt(totalMinute / 60);
let minute = totalMinute % 60;

console.log(hour + " " + minute);
```
