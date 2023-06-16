# 단어의 개수 문제 풀이

백준 1152 문제
(https://www.acmicpc.net/problem/1152)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/8e2c239e-fac2-48c0-b5d2-018142302044"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/bdf06d58-d9f2-4e97-aede-4fbe2d142b94"/></a>

<br/>
<br/>

## 내가 쓴 코드 (X)

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let word = input[0].split(" ");

console.log(word.length);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 문자열의 앞이나 뒤에 공백이 존재할 수 있으므로 trim() 메소드를 사용해준다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let word = input[0].trim().split(" ");

if (word == "") {
  console.log(0);
} else {
  console.log(word.length);
}
```
