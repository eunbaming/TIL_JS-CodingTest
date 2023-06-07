# 단어의 개수 문제 풀이

백준 1152 문제
(https://www.acmicpc.net/problem/1152)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/8427ed13-2887-4c46-b145-2f6140b05873"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/911ee08a-6290-4718-8400-d3c92a26ab64"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/a7f32654-5910-4f67-aa0f-a7630a33d973"/></a>

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
