# 그룹 단어 체커 문제 풀이

백준 1316 문제
(https://www.acmicpc.net/problem/1316)

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

let num = Number(input[0]);
let count = 0;
for (let i = 1; i <= num; i++) {
  let x = input[i].split("");

  for (let j = 0; j < x.length; j++) {
    if (x[j] === x[j + 1]) {
      x[j + 1].delete();
    }
  }
  let result = x.every((index, item) => index === x.indexOf(item));
  if (result === true) {
    count += 1;
  }
}

console.log(count);
```

<br/>
<br/>

## 선생님 해설

### 문제 해결 아이디어

- 집합자료형인 set함수를 사용하여 문제를 푼다.

```javascript
let fs = require("fs");
let input = fs.readFileSync("/dev/stdin").toString().split("\n");

// 그룹 단어인지 체크하는 함수
function checker(data) {
  let setData = new Set(data[0]);
  for (let k = 0; k < data.length - 1; k++) {
    // 오른쪽 단어와 다르다면
    if (data[k] != data[k + 1]) {
      // 이미 등장한 적이 있는 알파벳이라면
      if (setData.has(data[k + 1])) {
        return false;
      } else {
        setData.add(data[k + 1]);
      }
    }
  }
  return true;
}

let num = Number(input[0]);
let summary = 0;

for (let i = 1; i <= num; i++) {
  let inDdata = input[i];
  if (checker(inDdata)) {
    summary += 1;
  }
}

console.log(summary);
```
