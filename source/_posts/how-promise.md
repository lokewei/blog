---
title: how-promise
date: 2017-07-26 20:43:13
tags:
---
- `then`只是注册了一些后续的回调
- `resolve`执行后才会触发then注册的动作
- 使用`setTimeout(cb, 0)`保证注册的回调在event loop最尾部
