# 나머지 문제 풀이

백준 3052 문제
(https://www.acmicpc.net/problem/3052)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/23a6f960-e79e-4fbc-bb1d-81c88679c7ce"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/6511be61-66fc-4e67-98e5-03ada99cfc41"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/d1067e98-6d1c-4c51-87b9-3e06fe159f3b"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/d1e2b3a6-67f4-4f0c-acfa-a0f29bf47341"/></a>

<br/>
<br/>

## 내가 쓴 코드 (OX)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let arr = [];
for (let i = 0; i < 10; i++) {
  arr.push(Number(input[i]) % 42);
}

let result = arr.filter((item, index) => arr.indexOf(item) === index); // 처음에 알지 못했던 부분

console.log(result.length);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 중복되지 않은 수를 찾기 위해 집합자료형인 set함수를 사용한다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let data = input.map(Number);
let mySet = new Set(); // 집합 객체 생성

for (let i = 0; i < 10; i++) {
  mySet.add(data[i] % 42);
}

console.log(mySet.size);
```
