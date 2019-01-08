---
layout :    post
title :     What the differences between list.sort() and sorted(list)
data:       2019-01-08
author:     M.Shaw
catalog:    true
tag:
    Python
    
---
参考：[**click here**](https://stackoverflow.com/questions/22442378/what-is-the-difference-between-sortedlist-vs-list-sort)
list 算是Python中最重要的一种数据结构，用的最多，功能强大，及其方便，有很多Pythonic的操作
现在是涉及到list的排序，有两种方法：
* list.sort()
* sorted(list)
这两种方法都可以将list内部元素按照升序（默认为升序，如果要降序，需要将参数reverse设置,list.sort(reverse = True)排序.
###区别在于：
* list.sort() 是对list原地排序，也就是原来的顺序会被打乱，返回None(返回None这个地方容易被误用）
* sorted(list) 使用时会返回一个新的排序后的list，保持原来的list不变
sorted可以作用于任何可迭代的结构，例如还有strings, tuples, dictonaries(得到keys),generators等，然后返回一个元素排序后的list
### 使用：
* 如果你想把原始list的顺序排序，用list.sort(), 如果不想改变原list的元素顺序，使用sorted(list)
* 由于sorted(list)在调用过程中，是将创建的list副本排序返回，所以，list.sort() 比sorted(list)快
* list.sort() 一旦调用， 原list的顺序将不复存在
