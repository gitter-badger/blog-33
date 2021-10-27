---
title: DMIT 高防服务器评测
date: 2021-06-01 04:29:12
tags: 
- vps
- 评测
categories: 商家评测
---

DMIT，主营香港、洛杉矶大带宽VPS的国人商家，机器性能强悍，带宽充足，适合稳定建站，支持PayPal、支付宝、信用卡支付，不过价格也是非常美丽。
今天评测的是DMIT的高防洛杉矶VPS，提供了5Tbps+的无限制DDos防护。
<!--more-->

## 相关索引 ##
官网地址：https://www.dmit.io/
使用条款：https://www.dmit.io/pages/tos
购买链接：https://www.dmit.io/cart.php

## SSH连接 ##
之所以要在这里提一嘴，是因为这玩意不支持SSH密码登陆。
首次打开服务器管理面板的时候，会弹出一个下载私密金钥：
![QQ截图20210429171152.png][1]
如果错过了，只能重建一个，位置如图：
![QQ截图20210429172301.png][2]
这家的服务器只能用这个密钥登录，否则就只能用官方提供的noVNC登录.
下载完之后，打开这个zip，找到/private_key/id_rsa.pem，解压，这玩意就是你登录需要的东西。
然后打开你的SSH工具，这里以FinalShell为例
![QQ截图20210429171721.png][3]
![QQ截图20210429171827.png][4]
![QQ截图20210429171903.png][5]
然后选中id_rsa.pem，保存，然后返回
![QQ截图20210429171721.png][6]
这样不用输入密码就能登录了。
说完了，开始评测。

## 套餐详情 ##
 - 2x CPU核心
 - 2G 内存
 - 20G SSD硬盘
 - 1 IPv4 & 1 IPv6 /64
 - 200Mbps 带宽
 - 1000G 流量

## 测试详情 ##
| 项目     | 值                              |
| ---------- | -------------------------------- |
| 操作系统 | Ubuntu 18.04.5 LTS               |
| CPU型号  | AMD EPYC 7402P 24-Core Processor |
| CPU数量  | 2 vCPU                           |
| 虚拟化类型 | KVM                              |
| 内存用量 | 260.03 MB / 1.95 GB              |
| 硬盘用量 | 1.88 GB / 20.15 GB               |

## IP信息 ##
| 项目      | 值                                  |
| ----------- | ------------------------------------ |
| IPV4 ASN    | DMIT - DMIT Cloud Services, US       |
| IPV4 归属地 | United States California Los Angeles |
| IPV6 ASN    | DMIT - DMIT Cloud Services, US       |
| IPV6 归属地 | United States United States          |

## 流媒体解锁 ##
| 项目                         | 值 |
| ------------------------------ | --- |
| HBO Now                        | Yes |
| Bahamut Anime                  | No  |
| Abema.TV                       | No  |
| Princess Connect Re:Dive Japan | Yes |
| BBC                            | No  |
| Bilibili China Mainland Only   | No  |
| Bilibili Hongkong/Macau/Taiwan | No  |
| Bilibili Taiwan Only           | No  |

## CPU性能测试 (标准模式, 3-Pass @ 30sec) ##
单线程测试：1642 Scores
多线程测试：3236 Scores

## 内存性能测试 (标准模式, 3-Pass @ 30sec) ##
单线程读：39490.55 MB/s
单线城写：17708.81 MB/s

## 磁盘性能测试 (4K块/1M块, Direct写入) ##
| 测试项目   | 写速度                     | 读速度                      |
| -------------- | ----------------------------- | ------------------------------ |
| 100MB-4K Block | 38.3 MB/s (9353 IOPS, 2.74 s) | 52.4 MB/s (12785 IOPS, 2.00 s) |
| 1GB-1M Block   | 870 MB/s (830 IOPS, 1.20 s)   | 246 MB/s (234 IOPS, 4.27 s)    |

## Speedtest.net 网速测试 ##

| 测速节点 | 下载        | 上传        |
| -------- | ------------- | ------------- |
| 最近节点 | 102.98 Mbit/s | 99.93 Mbit/s  |
| 东京   | 76.55 Mbit/s  | 105.34 Mbit/s |
| 天津移动 | 100.57 Mbit/s | 100.12 Mbit/s |

  [1]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/798672619.png
  [2]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2709543711.png
  [3]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2139142268.png
  [4]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/969158875.png
  [5]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/23178470.png
  [6]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2139142268.png
