---
title: 宝塔安装 Misskey
date: 2021-06-04 15:04:39
updated: 2021-06-04 15:04:39
tags:
- 宝塔
- Misskey
categories: 简单记录
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108202234.png
---

本来看 Misskey 的安装文档，感觉没啥难的，但是我感觉我把能踩的坑全都踩了个遍，就导致我安了俩小时，中间服务器因为网络问题还断掉过一次 SSH，就挺崩溃的，所以必须记录一下了。
<!--more-->

### 安装 ###

1. 用宝塔面板插件，PostgreSQL 管理器，安装 PostgreSQL 10.5

2. 宝塔安装 Redis，在软件商店点安装就完事了

3. 用宝塔面板插件，PM2 管理器，安装 Node.js，12.x, 14.x 都可以

4. 安装 Yarn

   `npm install yarn -g`

5. 安装 postgres 的 npm 模块（我并不确定是否真的需要这步）

   `npm install postgres`

6. 克隆 Misskey 项目的 master 分支

   `cd /home && git clone -b master git://github.com/misskey-dev/misskey.git`

7. 安装 Misskey 的依赖

   `yarn`

8. 复制 .config/example.yml 并重命名为 default.yml

   `cp .config/example.yml .config/default.yml`

9. 编辑 default.yml，把 url 改一下

   ```yml
   To use option 1, uncomment below line.
   
   #port: 3000    # A port that your Misskey server should listen.
   ```

   再把上边第一个#号删除，3000 是端口可改可不改，然后数据库名称、用户名、密码，你在里边填写了，再去宝塔插件 PostgreSQL 管理器里边按照你填的信息创建数据库就行了，然后这个配置文件其他东西都是可管可不管的。

10. 构建 misskey

    ```bash
    apt install build-essential -y && NODE_ENV=production yarn build
    ```

11. 初始化数据库

    `yarn run init`

    如果报错，十有八九是坑比宝塔创建 psql 数据库出了毛病，同样操作，删除数据库再重新创，多试试就行了

12. 运行 Misskey

    `NODE_ENV=production npm start`

    如果运行无误，就 CTRL+C 退出

13. 后台运行 Misskey

    如果没装 screen 就`apt install screen -y`

    装了就直接一把梭：

    `screen && cd /home/misskey && NODE_ENV=production npm start`

    最后 CTRL+D 退出 screen，这样 Misskey 就自动在后台跑了

### 最后的最后 ###

一番使用下来，比 Mastodon 顺手多了，算是能养老的程序了（）
