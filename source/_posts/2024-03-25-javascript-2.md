---
title: JavaScript 入门（2）：编码练习
date: 2024-03-25 18:00:00
categories:
- [programming, javascript]
tags: 
- sum
- guess-number
- chickens-rabbits-problem
- perfect-number
- max
---

### 从 1 加到 100

```javascript
let a = 1
for (let i = 2; i <= 100; i++) {
  a = a + i
}
console.log(a)
```

### 猜数字

> 一个数除以 3 余 2，除以 4 余 3，除以 5 刚好除尽，这个数是几？

```javascript
for (let i = 1; i <= 100; i++) {
  if (i % 3 == 2 && i % 4 == 3 && i % 5 == 0) {
    console.log(i)
  }
}
```

### 鸡兔同笼问题

> 46 个头，128 只脚，请问鸡和兔分别有多少只？

```javascript
for (let i = 1; i <= 1000; i++) {
  for (let j = 1; j <= 1000; j++) {
    let heads = i + j
    let feet = i * 2 + j * 4
    if (heads == 46 && feet == 128) {
      console.log(i, j)
    }
  }
}
```

### 求解完全数

> 一个数的因数和等于自身，这个数可能是 6，28，下一个数是多少？

```javascript
for (let i = 1; i <= 10000; i++) {
  let x = 0
  for (let j = 1; j <= i - 1; j++) {
    if (i % j == 0) {
      x = x + j
    }
  }
  if (i == x) {
    console.log(i)
  }
}
```

### 找出数组中的最大值

```javascript
let a = [13, 5, 7, 9, 34, 16, 8]

function f(x) {
  let b = x[0]
  for (let i = 1; i < x.length; i++) {
    if (b < x[i]) {
      b = x[i]
    }
  }
  return b
}

let r = f(a)
console.log(r)
```