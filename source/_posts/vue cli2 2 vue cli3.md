---
title: 从 vue cli2 到 vue cli3
date: 2019-11-03 17:46:48
tags:
---
&emsp;&emsp;距离上一次已经过了一个多月了，flag果然不好实现。近期学习热情有点高涨，主要是要是不连续起来，前面看的东西，太容易忘了，下次看回忆部分就得很久了。
&emsp;&emsp;cli3看了挺久了，这两周终于草草过了一遍。
&emsp;&emsp;cli2和cli3的区别
&emsp;&emsp;cli2基本就是对webpack配置的preset，创建vue项目的时候，把复杂的webpack的基本配置已经做好了，剩下的个性化配置，就根据项目情况做一些特殊配置就好。比如：cli2会生成两个配置目录，config目录，用来配置项目的一些资源路径，项目端口号之类的；build目录，webpack的常用单页配置，拆分开发环境和生产环境，抽离两个环境公共配置，工具函数等等，整体来讲，比较容易理解。
&emsp;&emsp;cli3，本质上来讲，是对webpack的上一层封装。新建项目后，不在能看到webpack的相关的配置文件，只有项目文件。配置文件全部以npm包的形式组织到node_modules里面了。核心的两个插件@vue/cli + @vue/cli-service，一个是项目生产插件，一个是启动服务器插件，暴露出来的提供给使用者的可配选项在vue.config.js文件中。包括环境变量以及webpack插件的通用配置。封装了更有好的项目解决方案。文档里面的内容就不详细些了，大概列一下有哪些东西：vue自带插件以及自编插件方式、preset--预设置，项目启动的时候，安装之前保存的配置、build的时候，对针对目标浏览器的配置、静态资源输出的配置方式、css相关的预处理、webpack暴露出来的各种配置接口、通过不同模式来使用不同的环境变量、构建以及部署的解决方案等等。里面有很多不错的工程解决方案，一方面可以好好使用，另一方面也可以借鉴里面的解决思路，对以后面对类似的问题提供思路。
&emsp;&emsp;cli3的使用总结到这里，讨论一些深入的问题。后续需要看插件的开发方式，以及cli3的插件的组织方式。以及下一层的webpack的插件的开发方式以及插件的组织方式，猜测他们一定有共同点。需要的基础知识，包括node的常规知识，npm包的使用规则等。这些东西都是目前欠缺的。
&emsp;&emsp;cli3里面还有很多关于不同方向的处理方案，这些都还是盲点。简单的处理方案已经更深入的工程方面的解决方案的优劣等等。

ps：我太难了。。。