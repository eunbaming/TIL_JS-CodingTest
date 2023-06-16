# Stack 구현 (배열 자료형)

```javascript
let stack = [];

stack.push(5);
stack.push(4);
stack.push(3);
stack.pop();
stack.push(2);
stack.push(1);
stack.push(0);
stack.pop();

let reversed = stack.slice().reverse();

console.log(reversed); // 최상단 원소부터 출력
// [1, 2, 4, 5]
console.log(stack);
// [5, 4, 2, 1]
```
