---
title: JavaScript 入门（3）：排序算法
date: 2024-03-27 18:00:00
categories:
- [programming, javascript]
tags: 
- algorithm
- selection-sort
- quick-sort
---

我学了一些排序算法。

### 选择排序

```javascript
let a = [6, 4, 3, 5, 12, 10]
for (let i = 0; i < a.length - 1; i++) {
  for (let j = i + 1; j < a.length; j++) {
    if (a[j] < a[i]) {
      let t = a[j]
      a[j] = a[i]
      a[i] = t
    }
  }
}
debugger
```

### 快速排序

```javascript
let a = [6, 4, 3, 5, 12, 10]

function f(x) {
  if (x.length <= 1) {
    return x
  }

  let t = x[0]
  let l = []
  let r = []
  for (let i = 1; i < x.length; i++) {
    if (x[i] < t) {
      l.push(x[i])
    } else {
      r.push(x[i])
    }
  }

  let bl = f(l)
  let br = f(r)

  let e = [...bl, t, ...br]
  return e
}

let b = f(a)
debugger
```