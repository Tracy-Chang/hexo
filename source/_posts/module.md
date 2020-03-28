---
title: js中的模块化
date: 2019-11-29 16:11:22
tags:
---

这一点与 CommonJS 规范完全不同。CommonJS 模块输出的是值的缓存，不存在动态更新，详见下文《Module 的加载实现》一节。

CommonJS 运行时加载, es6 module 编译时加载 

import后面的from指定模块文件的位置，可以是相对路径，也可以是绝对路径，.js后缀可以省略。如果只是模块名，不带有路径，那么必须有配置文件，告诉 JavaScript 引擎该模块的位置。

import语句是 Singleton 模式

export和export default的区别


1.export：
   -直接输出（variable, function, class）,或者用大括号{}输出
   -存在动态更新，CommonJS不存在动态更新
   -可以在任何位置，只是需要在顶层
2.import:（静态执行）
   -引入的variable是只读的，引入对象可以改变，不建议更改
   -由于import是静态执行，所以不能使用表达式和变量
   -import命令具有提升效果
3.export default:(用来解决，import的时候，不用知道export的具体名字的)
   -import不需要大括号{},
   -不可以直接输出var定义方式
4.ES6 模块与 CommonJS 模块的差异：
   -CommonJS 模块输出的是一个值的拷贝，ES6 模块输出的是值的引用。
   -CommonJS 模块是运行时加载，ES6 模块是编译时输出接口。


   https://github.com/SunshowerC/blog/issues/8