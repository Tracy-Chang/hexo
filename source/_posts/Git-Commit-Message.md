---
title: Git-Commit-Message
date: 2020-04-06 15:47:37
tags:
---
## 优雅的 commit msg
##### 方案一 git-cz
* 安装 git-cz,执行 npx git-cz,生成 commit mgs。
* git-cz 地址：https://github.com/streamich/git-cz
* changelog.config.js 可以配置选择的时候，文案等内容

##### 方案二  commitizen/cz-cli + commitizen/cz-conventional-changelog
* 安装 npm install -D commitizen cz-conventional-changelog
* 将 commitizen 的作用地址指向 cz-conventional-changelog，作为 cli 的输出的选择内容。
* 修改 .czrc 或 package.json 中的 config 为:
```
{ "path": "cz-customizable" }
or
"config": {
    "commitizen": {
        "path": "node_modules/cz-customizable"
    }
}
```

## 校验 commit msg 的格式
##### 方案一 配个 vue 的 git hooks，来实现校验
```
gitHooks: {
    "commit-msg": "node scripts/verifyCommitMsg.js",
}
```

##### 方案二 commitlint
* 它需要一份校验的配置, 这里推荐 @commitlint/config-conventional 

## 生成 changelog
* standard-version 地址：https://github.com/conventional-changelog/standard-version
* 安装：npm i --save-dev standard-version
* 配置：
```
{
  "scripts": {
    "release": "standard-version"
  }
}
```
