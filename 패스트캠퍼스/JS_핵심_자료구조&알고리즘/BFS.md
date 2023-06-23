# BFS 구현

```javascript
class Queue {
  constructor() {
    this.items = {};
    this.headIndex = 0;
    this.tailIndex = 0;
  }

  enqueue(item) {
    this.items[this.tailIndex] = item;
    this.tailIndex++;
  }

  dequeue() {
    const item = this.items[this.headIndex];
    delete this.items[this.headIndex];
    this.headIndex++;
    return item;
  }

  peek() {
    return this.items[this.headIndex];
  }

  getLength() {
    return this.tailIndex - this.headIndex;
  }
}

let graph = [[], [2, 3, 4], [1], [1, 5, 6], [1, 7], [3, 8], [3], [4], [5]];

let visited = new Array(9).fill(false);

function bfs(graph, start, visited) {
  let queue = new Queue();
  queue.enqueue(start);
  visited[start] = true;
  while (queue.getLength() != 0) {
    let v = queue.dequeue();
    console.log(v);
    for (let i of graph[v]) {
      if (!visited[i]) {
        queue.enqueue(i);
        visited[i] = true;
      }
    }
  }
}

bfs(graph, 1, visited);

// 실행 결과 : 1 2 3 4 5 6 7 8
```
