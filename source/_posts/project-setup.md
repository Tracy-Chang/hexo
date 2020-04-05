---
title: project-setup
date: 2020-04-05 18:19:50
tags:
---
### .browserslistrc / .env / .env.dev / .env.production / .env.test

参考：https://tracy-chang.github.io/2020/03/28/vue-cli3-setup/

### .editorconfig
* EditorConfig 的配置文件
* EditorConfig 有助于维护跨多个编辑器和IDE从事同一项目的多个开发人员的一致编码风格。统一文本编辑器的风格。
* EditorConfig 前端常用 IDE（sublime，atom，vscode） 没有内置，需要安装对应插件，已统一代码风格。
* EditorConfig 的配置方式和适用说明：https://editorconfig.org/

### .gitignore / .gitattributes
* 不上传git地址的文件
* gitattributes 上传git的时候，统一各个系统和 IDE 的各种格式，例如行结尾时的回车。https://git-scm.com/docs/gitattributes

### .npmignore
* npm 发布包的时候，会忽略文件里面的内容，优先级大于 .gitignore

### .npmrc
* 用来配置存储 npm 的配置内容的，详细配置地址：https://docs.npmjs.com/using-npm/config

### .eslintrc / .eslintignore

参考：https://tracy-chang.github.io/2020/03/28/vue-cli3-setup/

### .babelrc.json / babel.config.js

参考：https://tracy-chang.github.io/2020/03/28/vue-cli3-setup/

### .postcssrc

### postcss.config.js

### jest.config.js

### changelog.config.js

### jsconfig.json

