---
title: CTF day 02
date: 2022-01-20 22:51:46
updated: 2022-01-20 22:51:46
tags:
- ctf
category: 学习笔记
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216230043.png
---

## 1.这不是 web 题

[这不是 web 题](http://chinalover.sinaapp.com/web2/index.html)

查看源码，没有有用信息，没引入任何文件，只有一张图片，于是

```bash
wget chinalover.sinaapp.com/web2/2.gif
```

右键查看属性，元信息里没有有价值的信息，那就看看二进制里头

```bash
strings 2.gif
```

输出信息末尾有个 `nctf{photo_can_also_hid3_msg}` ，解出来了

## 2.base64 decode/encode 的两种方式

```python
import base64 
base64.b64encode('something')
base64.b64decode('YmluYXJ5AHN0cmluZw==')
```

```bash
echo 'something' | base64
echo 'YmluYXJ5AHN0cmluZw==' | base64 -d
```