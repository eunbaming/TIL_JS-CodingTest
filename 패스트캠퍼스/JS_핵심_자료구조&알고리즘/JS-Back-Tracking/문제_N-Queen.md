# N-Queen 문제 풀이

N x N 체스 보드 위에 퀸 N개가 서로 공격할 수 없게 놓을 수 있는 가능한 모든 조합의 개수를 찾는 문제

## 문제 풀이

```javascript
let n = 8; // 전체 map 크기
let queens = []; // 현재 체스판에 놓인 queen의 위치 정보

// (x, y) 위치에 퀸을 놓을 수 있는지 확인
function possible(x, y) {
  for (let [a, b] of queens) {
    if (a === x || b === y) return false;
    if (Math.abs(a - x) === Math.abs(b - y)) return false;
  }
  return true;
}

let cnt = 0;
function dfs(row) {
  if (row === n) cnt++; //queen을 n개 배치할 수 있을 경우 카운트
  for (let i = 0; i < n; i++) {
    if (!possible(row, i)) continue;
    queens.push([row, i]);
    dfs(row + 1);
    queens.pop(); //  현재 위치에 퀸을 놓고 다음 단계로 넘어갈 때, 이전에 놓았던 퀸을 제거
  }
}
dfs(0);
console.log(cnt); // 92
```
