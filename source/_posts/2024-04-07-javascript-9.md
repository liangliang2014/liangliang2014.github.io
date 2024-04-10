---
title: JavaScript 入门（9）：树
date: 2024-04-07
categories:
- [Programming, JavaScript]
tags:
- data-structure
- tree
---

### 树的节点

树是一种数据结构，它是一个由 **节点** 组成的，具有层级关系的集合。
- 每个节点有 零或多个 **子节点**
- 没有 **父节点** 的节点，称为 **根节点**。除了根节点之外，每个节点有且只有一个父节点
- 除了根节点之外，每个子节点，可以构成多个不相交的 **子树**

{% asset_img tree.png %}

### 二叉树

- **二叉树** 是每个节点，最多有两个子节点（0、1、2）的树。

- **满二叉树**，每一层的每一个节点，都有两个子节点
{% asset_img full-binary-tree.png %}

- **完全二叉树**，中间节点都有两个子节点，最下层可以只有一个子节点（必须是左子节点）
- 满二叉树一定是完全二叉树，完全二叉树并不一定是满二叉树
{% asset_img complete-binary-tree.png %}

### 二叉树的遍历

{% asset_img traverse.png %}

#### 深度优先
- 前序遍历：中左右 `ABDECF`
- 中序遍历：左中右 `DBEAFC`
- 后序遍历：左右中 `DEBFCA`

```javascript
let a = {value: 'A'}
let b = {value: 'B'}
let c = {value: 'C'}
let d = {value: 'D'}
let e = {value: 'E'}
let f = {value: 'F'}

a.left = b
a.right = c
b.left = d
b.right = e
c.left = f
```

```javascript
function dfs(node) {
  if(node == null){
    return
  }

  let left = node.left
  let right = node.right
 
  // 调整后面三个语句的顺序，实现不同顺序的遍历
  // 中左右（当前）、左中右、左右中
  console.log(node.value)
  dfs(left)
  dfs(right)
}

dfs(a)
```

#### 广度优先

```javascript
function bfs(node) {
  let queue = [node]

  while (queue.length > 0) {
    let head = queue.shift()
    console.log(head.value)

    let left = head.left
    let right = head.right

    if (left != null) {
      queue.push(left)
    }
    if (right != null) {
      queue.push(right)
    }
  }
}

bfs(a)  // ABCDEF
```
