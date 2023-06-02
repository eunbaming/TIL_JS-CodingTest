# 평균은 넘겠지 문제 풀이

백준 4344 문제
(https://www.acmicpc.net/problem/4344)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/6a54ec80-4db1-441a-aa48-d48203628332"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/82e2a155-75ab-4d4f-9e7e-65c86385de08"/></a>

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let testCases = Number(input[0]);

for (let i = 1; i <= testCases; i++) {
  let data = input[i].split(" ").map(Number);
  let num = data[0]; // 학생 총 수
  let sum = 0; // 학생 점수 총합

  for (let i = 1; i <= num; i++) {
    sum += data[i];
  }

  let average = sum / num;
  let count = 0;

  for (let i = 1; i <= num; i++) {
    if (data[i] > average) count += 1;
  }

  console.log(`${((count / num) * 100).toFixed(3)}%`);
}
```
