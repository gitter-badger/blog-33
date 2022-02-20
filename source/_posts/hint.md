---
title: 优化 Windows 字体渲染
date: 2022-01-21 22:37:38
tags:
- Windows
- 字体渲染
- 优化
category: 简单记录
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216223516.png
---

尽管 Windows 在高分辨率屏幕上的字体渲染可圈可点，但是也不是所有电脑用户都能用上 4k 屏幕，我之前摸鱼用的笔记本是 Redmi pro 15，有一块 3.2k 的屏幕，我用久了，也没感觉 3.2k 屏幕有啥好，直到有一天，我购入了华硕天选 2，我的眼睛一瞬间失明了，于是我光速退货，换了台 ROG 幻 16，3.2k -> 2.5k 屏幕倒是没太难受，但是总感觉字体缺点味，于是我就开始了优化 Windows 字体渲染的路。

## 为什么 Windows 渲染拉跨

照理说，Windows 是市占率那么高的系统，Microsoft 那么有钱，没理由做不好区区一个字体渲染，被 Mac 疯狂吊锤，确实是有原因的。

（对这方面没有过多研究，如果有错误恳请各位大佬斧正）

Mac OS 的字体渲染机制跟 Windows 不太一样，Windows 讲究一个清晰（我知道这也许令人困惑，但是请你接着看完），因此 Windows 自带的荧幕字体平滑工具，叫做 cleartype 。本来低分辨率屏幕的字体显示效果就不太可能会好，然而 Windows 还非要让用户看清每一个笔画，甚至不惜让同一个字体里的字大小不一，就导致了各种奇葩的渲染效果。

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113191035.png)

而 MacOS 就采用了一种未曾设想的道路，它是将字体中笔画交叠的地方，直接弄得很模糊，然后加大渲染深度，让你看一眼，觉得还行。没 Mac 设备，用美化过的 Windows 代替一下：

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113190936.png)

而且搭载 Windows 系统的设备太多太杂，而且各种远古软件的历史包袱太重，因此 Microsoft 没有那个推翻重来的魄力（所以 Windows 再不重构就完了呀），然后字体渲染就一直摆烂，一直不改，到了今天这种情况。

## 那么如何改变呢

自然是有方法的，大致分为几步：

### 更换默认字体

微软雅黑在低分辨率屏幕上又不那么优秀，我们需要安装，并修改注册表，让应用默认使用比微软雅黑更优秀的更纱黑体。

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113192002.png)

#### 安装方法

1. 下载[更纱黑体](https://github.com/be5invis/Sarasa-Gothic/releases) 选择 sarasa-gothic-ttf-版本号.7z 这种，安装里头的 Sarasa UI SC regular 或者 semibold ，这个看个人喜好
2. 安装日本友人开发的 No!! MeiryoUI （东亚人民水深火热了属于是），替换字体，我的方案如下：![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113192438.png)

### 替换掉微软雅黑

很多软件自行指定了用微软雅黑（包括各种网页也是），那么偷偷把微软雅黑换掉，也是一个非常有效的办法。

我们选择安装微软曾经泄露，但是不知道为什么没启用的字体，Noble Scarlet (堕朱砂？)，它的标识都跟微软雅黑一模一样，所以直接安装就能替换微软雅黑。

下载地址：[goldkeyber 提供](https://github.com/goldkeyber112/noble-scarlet-mod) [我 fork 的](https://github.com/AkaraChen/noble-scarlet-mod)

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113191505.png)

### 更换渲染方式

上面的两个方式只是让渲染效果稍微好了一些，但是想要媲美 Mac OS，还得从根开始改，于是我们需要 Mactype 这款神器。

[下载](https://www.mactype.net/download.php?latest) Mactype，然后在配置引导里，选择服务加载，选择这个配置![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113193011.png)

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113193051.png)

即可配置完成，记得重启一下，让所有软件重新加载。

## 美化结果

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211113193411.png)

个人感觉效果还是非常不错的，比原来那种养眼多了