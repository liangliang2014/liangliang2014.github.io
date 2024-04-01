---
title: JavaScript 入门（2）
date: 2024-04-01
categories: programming
tags: 
- javascript
- language
---

### 一次定义多个变量

- 定义变量的同时，进行赋值

```javascript
let a = 1, b = 2
```

- 先定义，再赋值

```javascript
let a, b
a = 1
b = 2
```

### 更多循环

#### while 循环、do 循环

-  条件满足时，进行循环

```javascript
while (a < 10) {
  ...
}
```

- 先循环一次，条件满足则继续循环

```javascript
do {
  ...
} while (a < 10)
```

#### 循环控制

各种循环结构都可以，例如 `for`、`while`

- 退出循环

```javascript
while (a < 10) {
  ...
  break
}
```

- 进行下一轮循环

```javascript
while (a < 10) {
  ...
  continue
}
```

### 省略花括号

`if`、`for`、`while` 这些控制结构，当只有 **一行语句** 时，可以省略花括号（但是不推荐）

#### if 省略花括号

- 单独占一行

```javascript
if (a > 0)
  console.log('a > 0')
else
  console.log('a <= 0')
```

- 跟 `if`、`else` 放在一行

```javascript
if (a > 0) console.log('a > 0')
else console.log('a <= 0')
```

#### for 省略花括号

- 单独占一行

```javascript
for (let i = 0; i < 10; i++)
    console.log(i)
```

- 跟 `for` 放在一行

```javascript
for (let i = 0; i < 10; i++) console.log(i)
```

#### while 省略花括号

- 单独占一行

```javascript
while (a < 10)
  console.log(a)
```

- 跟 `while` 放在一行

```javascript
while (a < 10) console.log(a)
```
