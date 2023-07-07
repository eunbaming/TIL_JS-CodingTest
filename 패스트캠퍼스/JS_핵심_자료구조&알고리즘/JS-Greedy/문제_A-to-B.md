# A -> B 문제 풀이

백준 16953 문제
(https://www.acmicpc.net/problem/16953)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/5c8d1585-887e-4a86-9879-d7b130e38dd2"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/47656c4b-4ae6-4f6a-a8e9-0e6dee3fcc20"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/e0e3f3df-360f-4e12-88b2-8826507f8841"/></a>

<br/>
<br/>

## 문제 풀이

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let [a, b] = input[0].split(" ").map(Number);
let result = 1;
let flag = false;

while (a <= b) {
  if (a == b) {
    flag = true;
    break;
  }
  if (b % 2 == 0) b = parseInt(b / 2);
  else if (b % 10 == 1) b = parseInt(b / 10);
  else break;
  result++;
}

if (flag) console.log(result);
else console.log(-1);
```
