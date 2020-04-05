---
title: vue-preset
date: 2020-04-05 17:20:23
tags:
---
vue 的 preset 功能，可以帮助用户记录和保存一个项目的 init 情况，下次新增项目的时候，就可以直接使用之前的配置了。

#### 远程 preset
* preset.json: 包含 preset 数据的主要文件（必需）。
* generator.js: 一个可以注入或是修改项目中文件的 Generator。
* prompts.js: 一个可以通过命令行对话为 generator 收集选项的 prompts 文件。
* 项目运行过程中，preset 中的内容，代表 vue create 中预设的项目配置，generator 在预设内容安装完毕后，执行，可以新增文件和增加整合package.json中的 init 配置，prompts 负责提供对话框选择参数，传递给 generator 使用。

#### 使用方法：
```
vue create --preset username/repo my-project
```
* username 是指 github 的用户名
* repo 是指 github 的项目名