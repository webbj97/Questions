# 剑指Offer18. 删除链表的节点

> **JavaScript剑指Offer题解**<br>
> 🚀<font color=red>包含数组、对象、链表、堆栈、树等经典题型</font>
> ☕️每天一道，轻松不累
> 💬详细的题目解析，<font color=red>收藏</font>方便阅读
> 🙏[在线star地址](https://github.com/webbj97/fe-questions/tree/master/docs/algorithm)

### 在线阅读地址

<a href="https://github.com/webbj97/fe-questions/tree/master/docs/algorithm" target="blank">在线阅读地址</a>

### 题目描述

给定单向链表的头指针和一个要删除的节点的值，定义一个函数删除该节点。

返回删除后的链表的头节点。

注意：此题对比原题有改动


**示例 1:**

```
输入: head = [4,5,1,9], val = 5
输出: [4,1,9]
解释: 给定你链表中值为 5 的第二个节点，那么在调用了你的函数之后，该链表应变为 4 -> 1 -> 9.
```

**示例 2:**
```
输入: head = [4,5,1,9], val = 1
输出: [4,5,9]
```
解释: 给定你链表中值为 1 的第三个节点，那么在调用了你的函数之后，该链表应变为 4 -> 5 -> 9.

## 题解(遍历)

**思路**

1. 实际就是删除链表的某节点，比较基础。

```js
```js
/**
 * @param {ListNode} head
 * @param {number} val
 * @return {ListNode}
 */
var deleteNode = function(head, val){
	// 头节点找到值
    if(head.val == val) return head.next;
    let node = head;
    while(node.next){
        if(node.next.val!= val){
            node = node.next
        }else{
            node.next = node.next.next;
            break;
        }
    }
    return head;
};
```

 ## 写在最后

本篇是剑指Offer的第15题，俗话说好的合理的数据结构+算法才是写好代码的关键，不妨跟我一起来吧～

**热门开源项目**

* [前端进阶指南](https://github.com/webbj97/summary)
* [高频经典手撕代码实现](https://github.com/webbj97/fe-questions)
* [剑指Offer题解](https://github.com/webbj97/fe-questions/tree/master/docs/algorithm)


 