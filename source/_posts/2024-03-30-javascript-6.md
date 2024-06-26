---
title: JavaScript 入门（6）：集合与哈希表
date: 2024-03-30 18:00:00
categories:
- [programming, javascript]
tags: 
- data-structure
- set
- map
- hash-table
---

### JavaScript 中的集合

```javascript
let a = new Set()

a.add('x')          // 向集合中添加元素
let b = a.has('x')  // true，查找集合是否包含某个元素
```

#### 示例：判断数组中是否有重复元素

```javascript
let a1 = ['x', 'y', 'z', 'y']
let a2 = ['a', 'b']

function f(x) {
  let s = new Set()
  for (let i = 0; i < x.length; i++) {
    let e = x[i]
 
    // 一次判断每个元素是否在集合中，如果不在就加进去
    if (s.has(e)) {
      return true
    } else {
      s.add(e)
    }
  }

  return false
}

let r1 = f(a1)
let r2 = f(a2)
```


### JavaScript 中的哈希表

```javascript
let a = new Map()

a.set('gz', '甘蔗')   // 向哈希表中添加键值对
let b = a.get('gz')  // '甘蔗'，查找某个键对应的值
```

#### 示例：两数之和

```javascript
// https://leetcode.cn/problems/two-sum/description/

let nums = [3, 8, 0, 4]
let target = 7

function f(a, t) {
  let m = new Map()

  for (let i = 0; i < a.length; i++) {
    let b = t - a[i]
 
    // 依次判断每个数与目标值的差，是否在哈希表中
    // 如果不在，就把这个数与下标的映射关系，存到哈希表中
    if (m.has(b)) {
      let ii = m.get(b)
      return [ii, i]
    } else {
      m.set(a[i], i)
    }
  }
}

let r = f(nums, target)
```