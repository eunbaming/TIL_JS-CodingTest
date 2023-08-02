# N과 M(1) 문제 풀이

백준 15649 문제
(https://www.acmicpc.net/problem/15649)

<br/>
<br/>

## 문제

<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/84a0e7e2-10d8-4840-b28f-0e14a0199290"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/54103f57-d4c5-460e-bd89-dd31402916ea"/></a>
<a href="#"><img src="https://github.com/eunbaming/TIL_JS-CodingTest/assets/110072947/d82ba1a9-90b5-44f3-a357-77ced91349c9"/></a>

<br/>
<br/>

## 문제 풀이

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

// 자연수 n과 m
let n = Number(input[0].split(" ")[0]);
let m = Number(input[0].split(" ")[1]);
let arr = [];
for (let i = 1; i <= n; i++) {
  arr.push(i);
}
let visited = new Array(n).fill(false);
let selected = [];
let answer = "";

function dfs(arr, depth) {
  if (depth === m) {
    let result = [];
    for (let x of selected) result.push(arr[x]);
    for (let y of result) answer += y + " ";
    answer += "\n";
    return;
  }
  for (let i = 0; i < arr.length; i++) {
    if (visited[i]) continue;
    selected.push(i);
    visited[i] = true;
    dfs(arr, depth + 1);
    selected.pop();
    visited[i] = false;
  }
}
dfs(arr, 0);
console.log(answer);
```
