---
title: JavaScript 入门（5）：栈和队列
date: 2024-03-29
categories:
- [programming, javascript]
tags: 
- data-structure
- stack
- queue
---

### JavaScript 中的数组操作

```
unshift --> [] <-- push
shift   <-- [] --> pop
```

```javascript
let a = [1]

a.push(2)           // 右边进 [1,2]
a.unshift(3)        // 左边进 [3,1,2]

let b1 = a.pop()    // 右边出 2，剩下 [3,1]
let b2 = a.shift()  // 左边出 3，剩下 [1]
```

### 示例：栈 和 队列

| 数据结构 | 性质 | JavaScript 实现 |
| --- | --- | --- |
| 栈 | 先进后出 | `push, pop` 或 `unshift, shift` |
| 队列 | 先进先出 | `push, shift` 或 `unshift, pop` |

```javascript
// 栈
let stack = []

stack.push('hello')
stack.push('world')

// 先进后出
stack.pop()  // 'world'
stack.pop()  // 'hello'
```

```javascript
// 队列
let queue = []

quque.push('hello')
queue.push('world')

// 先进先出
queue.shift()  // 'hello'
queue.shift()  // 'world'
```