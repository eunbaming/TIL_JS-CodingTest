# 세자리 수 곱셈 문제 풀이

백준 2588 문제
(https://www.acmicpc.net/problem/2588)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/416157dd-1c89-4137-abc8-7fd946f0aadd"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/43227f58-fbb4-4443-ade3-711c5f0b4aa2"/></a>

<br/>
<br/>

## 내가 쓴 코드

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let a = parseInt(input[0]);
let b = input[1].split("");
let c = [];

for (let i = 0; i < b.length; i++) {
  c.push(parseInt(b[i]));
}

console.log(a * c[2]);
console.log(a * c[1]);
console.log(a * c[0]);
console.log(a * c[0] * 100 + a * c[1] * 10 + a * c[2]);
```

<br/>
<br/>

## 선생님 해설

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let a = input[0];
let b = input[1];

x_1 = b[2]; // 일의 자리
x_2 = b[1]; // 십의 자리
x_3 = b[0]; // 백의 자리

console.log(Number(a) * Number(x_1));
console.log(Number(a) * Number(x_2));
console.log(Number(a) * Number(x_3));
console.log(Number(a) * Number(b));
```
