# Merge-Sort (병합 정렬) 구현

```javascript
function merge(arr, left, mid, right) {
  let i = left;
  let j = mid + 1;
  let k = left;
  // sorted 배열 선언 및 초기화
  let sorted = new Array(right + 1);

  while (i <= mid && j <= right) {
    if (arr[i] <= arr[j]) sorted[k++] = arr[i++];
    else sorted[k++] = arr[j++];
  }
  // 왼쪽 배열에 대한 처리가 다 끝난 경우
  if (i > mid) {
    for (; j <= right; j++) sorted[k++] = arr[j];
  }
  // 오른쪽 배열에 대한 처리가 다 끝난 경우
  else {
    for (; i <= right; i++) sorted[k++] = arr[i];
  }
  // 정렬된 배열 결과를 원본 배열에 반영하기
  for (let x = left; x <= right; x++) {
    arr[x] = sorted[x];
  }
}

function mergeSort(arr, left, right) {
  if (left < right) {
    let mid = parseInt((left + right) / 2); // 2개의 부분 배열로 분한
    mergeSort(arr, left, mid); // 왼쪽 부분 배열 정렬 수행
    mergeSort(arr, mid + 1, right); // 오른쪽 부분 배열 정렬 수행
    merge(arr, left, mid, right); // 정렬된 2개의 배열을 하나로 병합
  }
}
```
