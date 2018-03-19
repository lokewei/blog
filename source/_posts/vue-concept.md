---
title: vue-concept
date: 2017-09-25 11:02:38
tags: vue
---
## 指令v-*
  - 对于直接输出html使用v-html
  - 对于标签自带的数据输出使用v-bind:[attr-name],简写:[attr-name]
  - v-on:submit.prevent，指令有修饰符可以简化一些固定套路,简写@click

## 生命周期
  - beforeCreate
  - created
  - beforeMount
  - mounted
  - beforeUpdate
  - updated
  - beforeDestroy
  - destroyed

## 单文件组件
  - .vue后缀
  - 使用template标签定义视图
  - 使用script放vue对象初始化
  - 使用style放组件自身的样式
