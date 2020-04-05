---
title: vue-cli3-setup
date: 2020-03-28 18:20:27
tags:
---
## .browserslistrc
##### introduction：
* 用来指定项目的目标浏览器的范围，会被babel转译。
* 指定方法：https://github.com/browserslist/browserslist

## babel
##### introduction：
* 配置方式：babel.config.js 或者 .babelrc.json
* 在babel.config.js中配置babel的配置项，babel封装在vue/cli-plugin-babel中。
* vue/cli-plugin-babel的配置方法：https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/babel-preset-app
* babel的配置方法：https://www.babeljs.cn/docs/

## eslint
##### introduction：
* 配置方式 .eslintrc.*
* 你可以通过在项目根目录创建一个 .eslintignore 文件告诉 ESLint 去忽略特定的文件和目录。
* 配置自带规则加插件规则，以及vscode插件，对项目中的代码进行规则校验。
* eslint的规则：https://cn.eslint.org/
* Vue + Vetur + ESlint + Prettier | ESlint + Prettier：简单的思路就是通过 Vetur 来做 Vue 代码风格的检查，比如template，style，Vetur 搭配 Eslint 检测 js 部分的代码风格， 调用 Prettier 进行代码风格的修正统一。
* 在安装之后，@vue/cli-service 也会安装 yorkie，它会让你在 package.json 的 gitHooks 字段中方便地指定 Git hook，可以在commit的时候执行eslint命令等。

##### Vscode 编辑器代码规范配置方案：
* 更新项目，并重新执行 npm i
* 安装 Vscode 插件： editorconfig, Vetur, Eslint, Prettier
* 打开项目的设置： Ctrl + , (Mac : Cmd + ,) ，选择工作区设置,打开 setting.json 文件，把下面插件相关的配置拷贝入文件，并保存
```javascript
{
    "eslint.validate": [{
        "language": "html",
        "autoFix": true
        },
        {
        "language": "vue",
        "autoFix": true
        },
        {
        "language": "javascript",
        "autoFix": true
        },
        {
        "language": "javascriptreact",
        "autoFix": true
        }
    ],
    "editor.formatOnSave": false,
    "eslint.autoFixOnSave": true,
    "vetur.validation.template": false,
}
```

##### env 环境变量和模式

通过使用 .env / .env[mode] 等文件，增加 mode 功能，可以传入不同 mode 下的对应变量。功能对应 webpack 的 mode 功能。
