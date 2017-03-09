---
title: js-void-0
date: 2017-03-09 19:13:08
tags:
---
今天见到js如下的值声明: var1: void 0，等价于: var1: undefined

#WTF 为啥要这么写？

原因：es5之前js里 undefined不是保留字，而是挂在globa对象上的一个属性可以被重新覆盖定义

> 参考: http://stackoverflow.com/questions/7452341/what-does-void-0-mean
