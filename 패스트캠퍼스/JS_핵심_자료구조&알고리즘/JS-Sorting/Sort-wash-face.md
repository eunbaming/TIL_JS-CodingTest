# 세수 정렬 문제 풀이

백준 4344 문제
(https://www.acmicpc.net/problem/2752)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/81f8e934-6735-451e-8f8c-3c97a4518ddb"/></a>

<br/>
<br/>

## 내가 쓴 코드 (X)

```javascript
let fs = require('fs');
let input = fs.readFileSync('/dev/stdin').toString().split('\n');

let [a, b, c] = input[0].split(' ').map(Number);
let result = [a, b, c];

result.sort((a, b) => return a- b);

console.log(result);
```

<br/>
<br/>

## 다시 푼 풀이

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let arr = input[0].split(" ").map(Number);

arr.sort((a, b) => a - b);

let answer = "";

for (let i = 0; i < arr.length; i++) {
  answer += arr[i] + " ";
}

console.log(answer);
```

<br/>
<br/>

## 선택 정렬로 푼 문제 풀이

```javascript
function selectionSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    let minIndex = i;
    for (let j = i + 1; j < arr.length; j++)
      if (arr[minIndex] > arr[j]) minIndex = j;
    let temp = arr[i];
    arr[i] = arr[minIndex];
    arr[minIndex] = temp;
  }
}

let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

let arr = input[0].split(" ").map(Number);
selectionSort(arr);

let answer = "";

for (let i = 0; i < arr.length; i++) {
  answer += arr[i] + " ";
}

console.log(answer);
```
