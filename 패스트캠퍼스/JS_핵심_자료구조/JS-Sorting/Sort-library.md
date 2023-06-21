# Sort library

## 정수에 대한 오름차순 정렬 예시

```javascript
let arr = [1, 8, 5, 9, 21, 3, 7, 2, 15];

// 예시 1
function compare(a, b) {
  if (a < b) return -1;
  else if (a > b) return 1;
  else return 0;
}

arr.sort(compare);
console.log(arr);

// 예시 2
function compare(a, b) {
  return a - b;
}

arr.sort(compare);
console.log(arr);

// 예시 3
arr.sort(function (a, b) {
  return a - b;
});

// 실행결과 : [1, 2, 3, 5, 7, 8, 9, 15, 21]
```

<br />
<br />

## 정수에 대한 내림차순 정렬 예시

```javascript
let arr = [1, 8, 5, 9, 21, 3, 7, 2, 15];

// 예시
arr.sort((a, b) => return b - a);
console.log(arr);

// 실행 결과 : [21, 15, 9, 8, 7, 5, 3, 2, 1]
```

<br />
<br />

## 문자열에 대한 오름차순&내림차순 정렬 예시

- 별도로 비교 함수(compare function)을 사용하지 않으면 유니코드 순으로 정렬된다.
- 함수를 적용하지 않음으로써, 간단히 문자열 정렬을 수행할 수 있다.

<br/>

- 오름차순 예시

```javascript
let arr = ["fineapple", "banana", "durian", "apple", "carrot"];

arr.sort();
console.log(arr);
```

<br />

- 내림차순 예시

```javascript
let arr = ["fineapple", "banana", "durian", "apple", "carrot"];

function compare(a, b) {
  if (a > b) return -1;
  else if (a < b) return 1;
  else return 0;
}

arr.sort(compare);
console.log(arr);

// 실행 결과 : ['fineapple', 'durian', 'carrot', 'banana', 'apple']
```

<br />

- 문자열에 대한 오름차순 예시 (대소문자 구분 X)

```javascript
let arr = ["fineapple", "Banana", "durian", "Apple", "carrot"];

function compare(a, b) {
  let upperCaseA = a.toUpperCase();
  let upperCaseB = b.toUpperCase();

  if (upperCaseA < upperCaseB) return -1;
  else if (upperCaseA > upperCaseB) return 1;
  else return 0;
}

arr.sort(compare);
console.log(arr);

// 실행 결과 : ['Apple', 'Banana', 'carrot', 'durian', 'fineapple']
```

<br />

- 객체에 대해 원하는 기준으로 내림차순 예시

```javascript
let arr = [
  { name: "홍길동", score: 90 },
  { name: "김철수", score: 85 },
  { name: "박영희", score: 97 },
];

function compare(a, b) {
  return b.score - a.score;
}

arr.sort(compare);
console.log(arr);

// 실행 결과
// [{ name: "박영희", score: 97 }, { name: "홍길동", score: 90 }, { name: "김철수", score: 85 }]
```
