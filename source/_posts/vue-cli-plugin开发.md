---
title: vue-cli-plugin
date: 2020-04-03 22:31:45
tags:
---
## vue-cli3插件内含文件

一个典型的 CLI 插件的目录结构看起来是这样的：
```
.
├── README.md
├── generator.js  # generator (可选)
├── prompts.js    # prompt 文件 (可选)
├── index.js      # service 插件
└── package.json
```

##### Service 插件
* 可以导出一个 server 命令，添加给 vue-cli-service。eg:vue-cli-service testcommand。
* 执行 vue-cli-service 命令的时候，可以改变 webpack 配置，去做对应的文件处理。
* 接收一个从 vue.config.js 文件中配置的参数，增加可配置性。

##### Generator
* generator 可以向 package.json 注入额外的依赖或字段。可用于通过 preset 生成项目的时候。
* 也可以向项目中添加文件。可用于，往项目中添加固定的模板代码的时候。
* template 渲染方式，EJS https://github.com/mde/ejs

##### Prompts
* 插件的对话框，可以提供参数的添加。这些参数会作为选项被传递给插件的 generator。
* 对话框的开发方式，https://github.com/SBoudrias/Inquirer.js