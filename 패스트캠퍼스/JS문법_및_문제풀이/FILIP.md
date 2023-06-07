# 상수 문제 풀이

백준 2908 문제
(https://www.acmicpc.net/problem/2908)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/88b2256a-1a92-449d-b1f5-428e8eab3326"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/7d81cdbf-eb2d-44f6-a04f-abfd166dc82a"/></a>

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let a = input[0].split(" ")[0];
let b = input[0].split(" ")[1];

let newA = a[2] + a[1] + a[0];
let newB = b[2] + b[1] + b[0];

console.log(Math.max(Number(newA), Number(newB)));
```
