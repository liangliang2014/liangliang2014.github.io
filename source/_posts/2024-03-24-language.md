---
title: JavsScript 小结
date: 2024-03-24
categories: programming
tags: 
- javascript
- language
---

最近我学了一门编程语言：[JavaScript](https://ecma-international.org/publications-and-standards/standards/ecma-262/)。

### 打印内容

```javascript
console.log(100)
console.log('Hello World')
```

### 变量

- 定义：`let a = 1`
- 使用：`a`
- 赋值：`a = 2`

### 表达式

- 相等：`==`
- 不相等：`!=`
- 大于：`a > 1`
- 大于等于：`a >= 1`
- 小于：`a < 1`
- 小于等于：`a <= 1`
- 并且：`&&`
- 或者：`||`
- 自增运算：`++`（`i++` 相当于 `i=i+1`）

### 控制结构

- 顺序：换行
- 选择：`if (a > 0) { ... }`
- 循环：`for (let i = 1; i <= 100; i++) { ... }`

### 数据类型

#### 简单数据类型

- 数字：`100` ...
- 字符串：`'Hello World'` ...
- 布尔值：`true`、`false`

#### 复合数据类型

- 数组
  - 定义：`let a = []`
  - 使用：`a[0]`
  - 赋值：`a[0] = 1`

- 对象
  - 定义：`let a = {}`
  - 使用：`a.b`（或者 `a['b']`）
  - 赋值：`a.b = 1`（或者 `a['b']=1`）

### 函数

- 定义：`function f(x) { ... return y }`
- 调用：`let b = f(a)`

### 一些数学知识

- 求余数：`5 % 2`
- 求绝对值：`Math.abs(x)`
