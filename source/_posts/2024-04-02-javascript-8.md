---
title: JavsScript 入门（8）：链表
date: 2024-04-02
tags:
- javascript
- data-structure
- linked-list
---

### 例子

```javascript
let node1 = { value: 1 }
let node2 = { value: 2 }
let node3 = { value: 3 }

node1.next = node2
node2.next = node3

// node1 -> node2 -> node3
let head = node1
```

### 链表操作

### 创建

```javascript
let a = ['苹果', '橘子', '香蕉']

function f(x) {
  let s = []

  for (let i = 0; i < x.length; i++) {
    let b = {
      value: x[i]
    }
    s.push(b)
  }

  for (let j = 0; j < x.length - 1; j++) {
    let u = s[j]
    let v = s[j + 1]
    u.next = v
  }

  let head = s[0]
  return head
}

let head = f(a)
```

### 遍历

```javascript
let c = head
while (c != null) {
  console.log(c.value)
  c = c.next
}
```

### 反转

```javascript
function f(head) {
  let a = null
  let b = head
  while (b != null) {
    let n = b.next
    b.next = a

    a = b
    b = n
  }
  return a
}

let r = f(head)
```