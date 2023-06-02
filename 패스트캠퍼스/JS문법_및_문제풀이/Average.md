# 평균 문제 풀이

백준 1546 문제
(https://www.acmicpc.net/problem/1546)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/379580bd-8892-4fe3-b2fb-710dfdeeb794"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/c647cdd0-69ce-482f-81c4-332142e84a5f"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/e8f7d583-9746-4a4b-8634-ff6170df26bf"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/99e1c749-c933-4fcd-916c-640b7708c02f"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/26266661-c0a9-49b4-8895-393041639ea7"/></a>

<br/>
<br/>

## 내가 쓴 코드 (O)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let num = Number(input[0]); // 시험 본 과목의 개수
let data = input[1].split(" ").map(Number);

data.sort((a, b) => b - a);
let max = data[0]; // 과목에서의 최댓값
// 위의 두 줄 대신에
// let max = Math.max(...data);
let result = 0;
for (let i = 0; i < data.length; i++) {
  result += (data[i] / max) * 100;
}

console.log(result / num);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- reduce함수를 사용하여 해결한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let num = Number(input[0]);
let scores = input[1].split(" ").map(Number);

let max = scores.reduce((a, b) => Math.max(a, b));
let updated = [];

for (let i = 0; i < num; i++) {
  updated.push((scores[i] / max) * 100);
}

console.log(updated.reduce((a, b) => a + b) / num);
```
