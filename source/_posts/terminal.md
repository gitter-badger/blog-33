---
title: 如何配置一个舒服的终端环境
date: 2021-11-08 18:57:12
tags:
---

## 前言

前几天趁着双11，购买了 ROG 幻 16，头一次用高端笔记本，我没下游戏测试（就算现在也没有），而是马上开始写起了代码，然而当我打开 Windows terminal 的那一刻，就看到了这么个界面：

![丑陋的 Powershell 啊](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main//20211108190420.png)

写代码的心情一下子消失了一半，于是就有了下面美化终端环境的过程。

## 你需要准备的

1. 能快速连接 GitHub 的网络环境
2. 一台 Windows 电脑
3. 一点点 vim 使用技巧

## 开始配置吧

> 说实话也没啥难的，主要是为了记录折腾的过程

### 装个包管理器

众所周知，各大 Linux 发行版都自带一个包管理器，能快速方便的安装软件，那么 Windows 上有吗？当然是有，除了 Windows 自带的图形化包管理器 Microsoft Store （啊，可能算是吧）外，还有 `scoop` 、 `chocolaty` 这种第三方包管理器，安装起来也是非常方便，用起来也跟 yum dnf apt 大差不离。

```
// 这是 scoop
iwr -useb get.scoop.sh | iex
```
```
// 这是 chocolaty
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

### 来个 neovim

在终端里有个趁手的编辑器还是很重要的，neovim 无疑是个很好的选择<del>（虽然我现在还是更喜欢 `code .`）</del>

有 scoop 的话可以很快速的解决

```
scoop install neovim
```

### 开始美化吧

安装好了包管理器和 neovim ，接下来就可以安装 oh-my-posh 来愉快的给 powershell 换主题了。

```
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
```

这样子就安装好了 oh-my-posh ，接下来是启用，并选中一个主题，我因为有喜欢的主题，就不过多阐述了，直接贴我的做法。

```
neovim $PROFILE
```

然后在里头输入

```
oh-my-posh --init --shell pwsh --config C:\Users\Akara\scoop\apps\oh-my-posh\6.0.0\themes\material.omp.json | Invoke-Expression
```

然后重启命令行，然后就变成了这样

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108192419.png)

反正是比之前好看多了

### 给 WSL 也美化一下

首先你需要开 WSL2
```
dism.exe /online /enable-feature /featurename:VirutalMachinePlatform /all /norestart
wsl --set-default-version 2
```

然后进入 WSL 的 bash 下

```
sudo apt install fish -y
which fish
chsh -s 输入你刚刚看到的 fish 路径
```

然后就配置好了，但是 fish 嘛，主要强在不用配置且功能强大，外观这东西实在是见仁见智，说实话，我觉得比 bash 好看，但是也没强到哪去，就不放图了

## 后话

简单配置一下子，至少比原来是舒服点的