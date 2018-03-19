---
title: wepack-hmr
date: 2017-10-23 16:10:15
tags:
---
webpack-dev-middleware 内存编译配合后端的express/koa使用，浏览器请求的文件路径会通过publicPath映射为内存里的文件
webpack-hot-middleware 在entry前面嵌入webpack-hot-middleware/client增加HMR运行时，配合HotModuleReplacementPlugin使用局部热替换
webpack/hot/dev-server 监听客户端的postMessage，webpackHotUpdate开头的信息触发module.hot.check
webpack/hot/only-dev-server 只检查更新过了的模块，不会触发整页刷新
webpack-hot-middleware/client 连接服务端的socket监听更新事件，触发webpackHotUpdate的postMessage
webpack-dev-server 起服务端的socket与client建立连接

webpack config: `devServer`
webpack.HotModuleReplacementPlugin

碰到的问题：
1. webpackHMR都配置ok，但是修改后还是整页刷新通过chrome preserve log查看是hot-update.json文件是按照当前页面路径的`./`来访问，但是webpack hmr生成的json文件是在项目根路径下，如果访问html容器页路径不是在根路径下就会出现这个问题
