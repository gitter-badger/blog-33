---
title: 在安卓板子上安装一个现代 IDE
date: 2021-10-30 12:34:04
tags:
---

## 前言

前段时间入手了一台华为 MatePad Pro，准备体验一下 HarmonyOS ，这几天感觉下来还是非常爽的。本来买来是准备配合 CloudStudio 好好写代码的，然后我流量因为用的太多被限速了，开 CloudStudio 都血慢，于是准备在板子上直接跑一个 Vscode ，于是就有了这篇文章。

## 安装前的准备

1. 一台 Android 5.0 以上的安卓板子
2. 能快速直连国外的网络环境
3. 一个能看得懂中文的眼睛

## 安装教程

我感觉挺简单的，写这篇主要是为了记录，防止以后重新到处找教程，目前就是用的华为板子写的这篇文章。

### 安装 Termux

直接去 [F-Droid](https://search.f-droid.org/?q=termux&lang=zh_Hans) 下载就行,还可以下个 Termux-Styling 美化一下 Termux。

不推荐使用旧版 Termux ，如果还在用旧版还是尽快升级吧。

### 安装 Ubuntu 虚拟机

Ubuntu 只是 **推荐** 配置，具体用啥还得看你自由发挥,Debian肯定也是行的，CentOS 估计就不用看这个教程了。

下面用到的命令来自 [AnLinux](https://f-droid.org/zh_Hans/packages/exa.lnx.a/)

```
pkg install wget openssl-tool proot -y 
hash -r 
wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh 
bash ubuntu.sh 
```

直接复制到终端就能运行，运行完之后在当前窗口运行 ./start-ubuntu.sh 就能跑起来 Ubuntu

建议来一次系统更新助兴：

```
apt update && apt upgrade -y
```

### 安装 Node.js 14.x

官方推荐使用这个版本，事实上你也必须使用这个版本，否则安装的时候会直接报 Node 版本不匹配，而 Termux 仓库刚好删除了 `nodejs` 和 `nodejs-lts` 两个包的历史版本，直接在 Termux 添加 Node 官方源脑瘫问题也很多的样子（或许只是因为我懒得挨个解决？），所以你才必须安装虚拟机，然后这虚拟机问题又很多，于是你又必须通过 npm安装

```
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs
```

运行完之后用 `node -v` 看看有没有安装成功。

由于未知的原因，我在 Ubuntu 下始终无法用 npm 安装 yarn ，所以我来了波虚空操作，安装 cnpm ，然后用 cnpm 安装 yarn ，居然成功了

```
npm install -g cnpm --registry=https://registry.npm.taobao.org
cnpm install yarn -g
```

### 安装剩下的依赖，然后运行吧

```
sudo apt-get install -y \
  build-essential \
  pkg-config \
  python3
npm config set python python3
```

依赖安装完就要进行这玄学的安装了

```
yarn global add code-server
code-server
```

如果运行不了 `code-server` 就多安装一次，反正我第二次就成了...安装时间很长，要等很久，毕竟安卓平板的性能嘛，懂得都懂。

然后打开 localhost:8080 ，就能看到你的 code-server 了

## 结尾

啊，我又水了一篇，折腾从未停止，学习从未开始

我是 AkaraChen ，一个立志成为全栈神仙的人（做不到）