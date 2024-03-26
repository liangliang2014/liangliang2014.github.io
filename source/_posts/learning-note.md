---
title: 编程学习总结
date: 2024-03-25 20:47:43
tags:
---

### 编辑器

我学会了使用 [VSCode](https://code.visualstudio.com/) 编辑器。

![](https://code.visualstudio.com/assets/home/home-screenshot-mac-2x.png)

| 操作 | 快捷键 |
| --- | --- |
| 新建文件 | `⌘ + n` |
| 保存 | `⌘ + s` |
| 撤销 | `⌘ + z` |
| 反撤销 | `⇧ + ⌘ + z` |
| 格式化 | `⇧ + ⌥ + f` |
| 注释 | `⌘ + /` |
| 打开内置命令行 | `` ⌃ + ` `` |
| 复制 | `⌘ + c` |
| 剪切 | `⌃ + x` |
| 粘贴 | `⌃ + v` |

### 命令行

我还学了一些命令行操作。

![](https://iterm2.com/img/logo2x.jpg)

| 操作 | 命令 |
| --- | --- |
| 跳转到目录 | `$ cd <directory>` |
| 列出目录下的文件 | `$ ll` |
| 新建 Project | `$ npm init` |
| 安装依赖 | `$ npm install [-S] <pkg-name>` |
| 安装 `trash` 命令 | `$ npm install -g trash-cli` |
| 把文件丢入废纸篓 | `$ trash <file>` |

### 三、编程语言

我学会了一门编程语言：JavaScript。

#### 打印内容

```javascript
console.log(100)
console.log('Hello World')
```

#### 变量

- 定义：`let a = 1`
- 使用：`a`
- 赋值：`a = 2`

#### 表达式

- 相等：`==`
- 不相等：`!=`
- 大于：`a > 1`
- 大于等于：`a >= 1`
- 小于：`a < 1`
- 小于等于：`a <= 1`
- 并且：`&&`
- 或者：`||`

#### 控制结构

- 顺序：换行
- 选择：`if (a > 0) { ... }`
- 循环：`for (let i = 1; i <= 100; i++) { ... }`

#### 数据类型

##### 简单数据类型

- 数字：`100` ...
- 字符串：`'Hello World'` ...
- 布尔值：`true`、`false`

##### 复合数据类型

- 数组
  - 定义：`let a = []`
  - 使用：`a[0]`
  - 赋值：`a[0] = 1`

- 对象
  - 定义：`let a = {}`
  - 使用：`a.b`
  - 赋值：`a.b = 1`

#### 函数

- 定义：`function f(x) { ... return y }`
- 调用：`let b = f(a)`

#### 一些数学知识

- 求余数：`5 % 2`
- 求绝对值：`Math.abs(x)`

### 编程练习

我还进行了一些编程题目的学习。

#### 从 1 加到 100

```javascript
let a = 1
for (let i = 2; i <= 100; i++) {
  a = a + i
}
console.log(a)
```

#### 猜数字

> 一个数除以 3 余 2，除以 4 余 3，除以 5 刚好除尽，这个数是几？

```javascript
for (let i = 1; i <= 100; i++) {
  if (i % 3 == 2 && i % 4 == 3 && i % 5 == 0) {
    console.log(i)
  }
}
```

#### 鸡兔同笼问题

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

#### 求解完全数

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

#### 找出数组中的最大值

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