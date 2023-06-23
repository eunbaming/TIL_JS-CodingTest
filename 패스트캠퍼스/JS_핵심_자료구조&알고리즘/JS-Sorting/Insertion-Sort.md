# Insertion-Sort (삽입 정렬) 구현

```javascript
function insertionSort(arr) {
  for (let i=; i<arr.length; i++) {
    for (let j=i; j<0; j--) {
      if (arr[j] < arr[j-1]) {
        let temp = arr[j];
        arr[j] = arr[j-1];
        arr[j-1] = temp;
      } else if {
        // 자신보다 작은 데이터를 만나면 그 위치에서 멈춘다.
        break;
      }
    }
  }
}
```
