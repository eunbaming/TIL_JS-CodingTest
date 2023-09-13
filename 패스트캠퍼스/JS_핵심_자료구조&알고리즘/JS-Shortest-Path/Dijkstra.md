# 다익스트라(Dijkstra) 최단 경로 알고리즘 구현

```javascript
function dijkstra() {
  // Min Heap
  let pq = new PriorityQueue((a, b) => b[0] - a[0]);
  // 시작 노드로 가기 위한 최단 거리는 0으로 우선순위 큐에 삽입
  pq.enq([0, start]);
  distance[start] = 0;
  while (pq.size() != 0) {
    // 최단 거리 노드에 대한 정보 꺼내기
    let [dist, now] = pq.deq();
    // 현재 노드가 이미 처리된 적이 있다면 무시
    if (distance[now] < dist) continue;
    // 현재 노드와 연결된 다른 인접한 노드들을 호가인
    for (let i of graph[now]) {
      let cost = dist + i[1];
      if (cost < distance[i[0]]) {
        distance[i[0]] = cost;
        pq.enq([cost, i[0]]);
      }
    }
  }
}

let INF = 1e9;
// 노드의 개수 n
let n = 7;
// 시작 노드 번호 start
let start = 1;
let graph = [
  // 각 간선은 [노드, 비용]의 형태
  [],
  [
    [2, 3],
    [3, 1],
    [4, 2],
  ],
  [
    [1, 3],
    [3, 1],
    [5, 1],
  ],
  [
    [1, 1],
    [2, 1],
    [4, 3],
    [6, 5],
  ],
  [
    [1, 2],
    [3, 3],
    [7, 1],
  ],
  [
    [2, 1],
    [6, 2],
  ],
  [
    [3, 5],
    [5, 2],
  ],
  [[4, 1]],
];

let distance = new Array(n + 1).fill(INF);

dijkstra();

for (let i = 1; i <= n; i++) {
  if (distance[i] == INF) console.log("INFINITY");
  else console.log(distance[i]);
}
```
