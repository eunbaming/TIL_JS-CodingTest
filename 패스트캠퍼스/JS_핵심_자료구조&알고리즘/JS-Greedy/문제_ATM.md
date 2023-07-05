# ATM 문제 풀이

백준 1427 문제
(https://www.acmicpc.net/problem/11399)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/3fbaa123-cbdc-428f-91da-f085160d727a"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/50fe0ca8-4047-402f-81ae-cc8509596e5b"/></a>

<br/>
<br/>

## 나의 문제 풀이

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let n = Number(input[0]);
let arr = input[1].split(" ").map(Number);

arr.sort((a, b) => a - b);

let total = 0;
let time = 0;
for (let i = 0; i < arr.length; i++) {
  time += arr[i];
  total += time;
}

console.log(total);
```
