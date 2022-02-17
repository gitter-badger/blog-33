---
title: 安装 AdGuardHome 屏蔽广告
date: 2021-06-04 06:35:36
tags:
- AdGuardHome
- 广告
categories: 简单记录
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108201927.png
---

AdGuardHome 可以为您和您的设备提供隐私保护中心，是一个开源、免费、强大的去广告/跟踪器 DNS 服务器。
<!--more-->

我这里用的是腾讯云轻量应用服务器，广州地域，响应速度肯定是比大厂慢的，但是以后可以免受国内大数据的采集，这么看就香起来了。

### 如果你用腾讯云 ###

最好先把监控服务删了，腾讯云监控服务几分钟刷了 2500 个 DNS 查询，AdGuardHome 控制面板占比最多就是这个，烦的要死。

`/usr/local/qcloud/stargate/admin/uninstall.sh && /usr/local/qcloud/YunJing/uninst.sh && /usr/local/qcloud/monitor/barad/admin/uninstall.sh`

肯定要用 Root 用户的，不然权限不够

### 安装过程 ###

直接一行命令完事，不多 BB

`wget https://github.com/AdguardTeam/AdGuardHome/releases/download/v0.106.3/AdGuardHome_linux_amd64.tar.gz && tar xvf AdGuardHome_linux_amd64.tar.gz && cd AdGuardHome  && sudo chmod u+x AdGuardHome  && sudo ./AdGuardHome -s install`

全都跑完之后，打开你的服务器 IP:3000，然后就是傻瓜式安装向导

监听接口端口推荐跑 3000

> listen udp 0.0.0.0:53: bind: address already in use

如果看到这个错误提示，旁边有个修复，点一下就行

剩下就剩个创建管理员账户，按自己需求发挥就行，剩下就无脑 next 就行了。

安装完了，进入控制面板之后，还没代表能用，还要接着配置一下才能用。

### 本地化配置 ###

这玩意是国外的东西，不太适应中国国情，因此想要在国内用的爽，还需要自己添加一点规则。

到设置->DNS 设置中，删掉上游 DNS 服务器中的内容，填写如下内容：

```plain
223.5.5.5
223.6.6.6
119.29.29.29
182.254.116.116
tls://223.5.5.5
tls://223.6.6.6
tls://dns.pub
https://doh.pub/dns-query
```

同样删掉 Bootstrap DNS 服务器中的内容，写入如下内容：

```plain
9.9.9.10
149.112.112.10
2620:fe::10
2620:fe::fe:10
```

划到下方，测试上游 DNS，应该是没啥问题，然后点应用就行

然后打开过滤器->DNS 封锁清单，挨个添加阻止列表，名字随便填，链接要一个一个添加

```plain
https://
```

然后差不多就能用了。

### 可选配置：DNS-over-HTTPS ###

整完之后就能给安卓 Pie 引入的私人 DNS 功能使用了，这样以后安卓端无论练什么 WiFi 都能自动配置 DNS，方便。

打开管理面板->设置->加密设置，打勾，然后其他保持默认，填你的域名，然后填写证书啥的就能一键启用了，很方便。
