---
title: 记录一下 node-gyp 报错的问题
date: 2022-02-16 23:37:38
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216225817.png
---

## node-gyp 是个啥

gyp 是为 Chromium 项目创建的项目生成工具，可以从平台无关的配置生成平台相关的项目文件。这样一来我们就不需要花额外的时间处理每个平台不同的项目配置以及项目之间的依赖关系。

啊，说人话就是，拿来编译 C++ 扩展的。

## 前因

今天接了个活，`npm install` 的时候显示 node-gyp 报错，一下子爆了几十行错，隐约看到了数个 node-gyp 的字眼，让我一下子想起了半年前的夏天我魔改 hexo 主题也看过这个报错，然而当时我知难而退，然而现在这是手里有活，不能 run 了(悲)

## 分析下报错

```bash
verb check python checking for Python executable "python2" in the PATH
```

嗯，熟悉的 python 报错，还是当年那个味，说到底 node 项目还要引用 python 真的就挺离谱的，真的。

根据报错原因我去下了 python 2.7，Windows 下载地址在[这里](https://www.python.org/downloads/release/python-2718/)

然而之后的报错日志还有一大截，按理说应该就从这里停了啊？我发觉不对，接着往下翻，找到这个报错：

```python
import sys; print "%s.%s.%s" % sys.version_info[:3];
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
SyntaxError: Missing parentheses in call to 'print'. Did you mean print(...)?
```

我超，熟悉的 python 的报错提示，然后我迷惑了，print 函数不加括号要怎么跑？ Chromium 团队写 python 能写出这种离谱东西吗？

然后我顺着报错面向 Google 编程了一下，StackOverflow 上的回答告诉我这是 python 2 特有的写法，在 python 3 上已经被移除了。

也就是说，node-gyp 安装的时候会默认找 python2，如果找不到那就去找其他 python，然后就找到了我装的 Anaconda，最后导致的报错。

## 如何解决

既然如此，解决方案就很明了了，无非几步：

1. 安装 python 2.7
2. 告知 node 应该使用 python 2.7
3. 最后成功安装 node-gyp，把项目跑起来

经过一番 Google 后，还是让我找到解决方法了，<del>举办辣</del>。

设置 node 默认使用 python 2.7：

```bash
npm config set python python2.7
```

然后就能 `npm install` 了，问题解决
