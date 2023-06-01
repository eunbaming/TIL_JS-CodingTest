# 빠른 A+B 문제 풀이

백준 15552 문제
(https://www.acmicpc.net/problem/15552)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/41e26825-f02b-4131-ba31-6659d9379134"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/22fefa39-24a4-4234-a1c4-b67e0837be0e"/></a>

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 빠르게 출력하기 위해 하나의 문자열 변수에 정보를 담은 후 한꺼번에 문자열을 출력한다.
- 한 줄을 출력할 때마다 console.log()를 사용하면 많은 시간이 소요되므로 모든 줄에 대한 정보를 하나의 문자열에 담았다가 한꺼번에 출력한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let testCase = Number(input[0]);
let answer = "";

for (let i = 1; i <= testCase; i++) {
  let data = input[i].split(" ");
  let a = Number(data[0]);
  let b = Number(data[1]);

  answer += a + b + "\n";
}

console.log(answer);
```
