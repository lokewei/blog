---
title: react-setState-async-why
date: 2017-08-30 00:50:11
tags:
---
一次`setState`保证了当前函数栈里只会有最终的一次渲染，使用类似事务的方式锁住更新通道保证整个调用栈结束时才真正去渲染真实dom;
