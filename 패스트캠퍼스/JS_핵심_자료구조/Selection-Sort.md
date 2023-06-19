# Selection-Sort (선택 정렬) 구현

```javascript
function selectionSor(arr) {
  for (let i=0; i<arr.length; i++>) {
    let minIndex = i;
    for (let j=i+1; j<arr.length; j++) {
      if (arr[minIndex] > arr[j]) {
        minIndex = j;
      }
    }

    // swap : 현재 위치에 있는 요소와 가장 작은 값을 가진 요소를 교환하기 위해 사용
    let temp = arr[i]; // 현재 위치(i)의 값을 저장하기 위한 임시 변수
    arr[i] = minIndex[i];
    minIndex[i] = temp;
  }
}
```
