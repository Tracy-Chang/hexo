---
title: shell
date: 2020-04-25 15:09:53
tags:
---
### Shell 是一个应用程序
* Shell 是一个应用程序，它连接了用户和 Linux 内核，让用户能够更加高效、安全、低成本地使用 Linux 内核，这就是 Shell 的本质。
* Shell 还能连接其它程序

### Shell 是一种脚本语言
* Shell 并不是简单的堆砌命令，我们还可以在 Shell 中编程。站在这个角度讲，Shell 也是一种编程语言，它的编译器（解释器）是 Shell 这个程序。

> 我们平时所说的 Shell，有时候是指连接用户和内核的这个程序，有时候又是指 Shell 编程。

### 最常用的shell
在Linux 和 UNIX系统里可以使用多种不同的shell可以使用。最常用的几种是 Bourne shell (sh), C shell (csh), 和 Korn shell (ksh)。三种shell 都有它们的优点和缺点。Bourne shell 的作者是 Steven Bourne。它是 UNIX 最初使用的shell 并且在每种 UNIX 上都可以使用。Bourne shell 在 shell 编程方面相当优秀，但在处理与用户的交互方面作得不如其他几种 shell。

C shell 由 Bill Joy 所写，它更多的考虑了用户界面的友好性。它支持象命令补齐（command-line completion）等一些 Bourne shell 所不支持的特性。普遍认为C shell 的编程接口做的不如 Bourne shell, 但 C shell 被很多 C  程序员使用因为 C shell的语法和 C语言的很相似，这也是C shell名称的由来。

Korn shell (ksh) 由 Dave Korn 所写。它集合了C shell 和 Bourne shell 的优点并且和 Bourne shell 完全兼容。

除了这些 shell 以外，许多其他的 shell 程序吸收了这些原来的 shell 程序的优点而成为新的 shell 。在 Linux 上常见的有 tcsh (csh 的扩展)，Bourne Again shell(bash, sh 的扩展), 和Public Domain Korn shell (pdksh, ksh 的扩展)。bash 是大多数Linux 系统的缺省 shell。

### The Bourne Again Shell
Bourne Again shell (bash), 正如它的名字所暗示的，是 Bourne shell 的扩展。bash 与 Bourne shell 完全向后兼容，并且在 Bourne shell 的基础上增加和增强了很多特性。bash 也包含了很多 C 和 Korn shell 里的优点。bash 有很灵活和强大的编程接口，同时又有很友好的用户界面。

为什么要用 bash 来代替 sh 呢？Bourne shell 最大的缺点在于它处理用户的输入方面。在 Bourne shell 里键入命令会很麻烦，尤其当你键入很多相似的命令时。而 bash 准备了几种特性使命令的输入变得更容易。

### shell 选择
zsh、oh-my-zsh

查看系统当前使用的shell
```shell
$ echo $SHELL 
/bin/bash
```

查看系统是否安装了zsh
```shell
$ cat /etc/shells 
/bin/sh
/bin/bash
/sbin/nologin
/usr/bin/sh
/usr/bin/bash
/usr/sbin/nologin
/bin/tcsh
/bin/csh
```

切换shell为zsh
```shell
$ chsh -s /bin/zsh
Changing shell for root.
Shell changed.
```

参考链接：
shell: http://c.biancheng.net/view/706.html
bash: https://blog.csdn.net/wenlifu71022/article/details/4069929
shell选择：https://www.jianshu.com/p/d194d29e488c