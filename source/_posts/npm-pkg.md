---
title: npm-pkg
date: 2020-04-05 14:58:15
tags:
---
## npm 发布包的注意事项

* scope 创建，需要在npm官网先新建一个 scope，然后在 pkg 的 package.json 中的 name 属性中添加 scope，就可以发布到对应的 scope 下了。
* publish
```
npm publish --access public // 将权限公开
```

* unpublish
```
npm unpublish packagename --force
```