# Priority Queue - Heap 구현

```javascript
var PriorityQueue = require("priorityqueuejs");

// Max Heap
var queue = new PriorityQueue(function (a, b) {
  return a.cash - b.cash;
});

queue.enq({ cash: 250, name: "Valentina" });
queue.enq({ cash: 300, name: "Jano" });
queue.enq({ cash: 150, name: "Fran" });
queue.size(); // 3
queue.peek(); // { cash: 300, name: 'Jano' }
queue.deq(); // { cash: 300, name: 'Jano' }
queue.size(); // 2
```

<br/>
<br/>

출처 : https://github.com/ndb796/priorityqueuejs
