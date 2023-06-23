# Binary Search 구현

<br/>
<br/>

- 재귀 함수

```javascript
function binarySearch(arr, target, start, end) {
  if (start > end) return -1; // 데이터 존재 X
  let mid = parseInt((start + end) / 2);
  // 찾은 경우 중간점 인덱스 반환
  if (arr[mid] == target) return mid;
  // 중간점의 값보다 찾고자 하는 값이 작은 경우 왼쪽 학인
  else if (arr[mid] > target) return binarySearch(arr, target, start, mid - 1);
  // 중간점의 값보다 찾고자 하는 값이 큰 경우 오른쪽 학인
  else return binarySearch(arr, target, mid + 1, end);
}

// n(원소의 개수)와 target(찾고자 하는 값)
let n = 10;
let target = 7;
let arr = [1, 3, 5, 7, 9, 11, 13, 15, 17, 19];

// 이진 탐색 수행 결과 출력
let result = binarySearch(arr, target, 0, n - 1);
if (result == -1) console.log("원소가 존재하지 않습니다.");
else console.log(`${result + 1}번째 원소입니다.`);
```

<br/>
<br/>

- 반복문

```javascript
function binarySearch(arr, target, start, end) {
  while (start <= end) {
    let mid = parseInt((start + end) / 2);
    if (arr[mid] == target) return mid;
    else if (arr[mid] > target) end = mid - 1;
    else start = mid + 1;
  }
  return -1;
}

// n(원소의 개수)와 target(찾고자 하는 값)
let n = 10;
let target = 7;
let arr = [1, 3, 5, 7, 9, 11, 13, 15, 17, 19];

// 이진 탐색 수행 결과 출력
let result = binarySearch(arr, target, 0, n - 1);
if (result == -1) console.log("원소가 존재하지 않습니다.");
else console.log(`${result + 1}번째 원소입니다.`);
```
