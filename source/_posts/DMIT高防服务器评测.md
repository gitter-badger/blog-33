---
title: DMIT高防服务器评测
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

## 路由追踪测试 ##

    Traceroute to China, Beijing CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 123.125.99.1 (123.125.99.1), 30 hops max, 32 byte packets
     1  154.17.0.1  14.34 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.37 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.47 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.189.37  127.21 ms  *  China, ChinaTelecom
     5  *
     6  *
     7  59.43.80.102  135.57 ms  *  China, ChinaTelecom
     8  *
     9  *
    10  *
    11  219.158.3.77  179.67 ms  AS4837  China, ChinaUnicom
    12  125.33.186.94  175.41 ms  AS4808  China, Beijing, ChinaUnicom
    13  221.219.202.254  171.81 ms  AS4808  China, Beijing, ChinaUnicom
    14  124.65.194.50  168.93 ms  AS4808  China, Beijing, ChinaUnicom
    15  *
    16  *
    17  *
    18  123.125.99.1  166.62 ms  AS4808  China, Beijing, ChinaUnicom
    
    
    Traceroute to China, Beijing CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 180.149.128.9 (180.149.128.9), 30 hops max, 32 byte packets
     1  154.17.0.1  8.96 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.42 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.41 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.181.145  122.53 ms  *  China, ChinaTelecom
     5  59.43.247.141  231.58 ms  *  China, ChinaTelecom
     6  *
     7  59.43.132.17  149.93 ms  *  China, ChinaTelecom
     8  *
     9  36.110.244.46  159.50 ms  AS23724  China, Beijing, ChinaTelecom
    10  36.110.246.198  171.45 ms  AS23724  China, Beijing, ChinaTelecom
    11  180.149.128.9  149.25 ms  AS23724  China, Beijing, ChinaTelecom
    
    
    Traceroute to China, Beijing CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.136.25.153 (211.136.25.153), 30 hops max, 32 byte packets
     1  154.17.0.1  21.06 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.36 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  3.00 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.184.153  127.31 ms  *  China, ChinaTelecom
     5  59.43.187.81  128.22 ms  *  China, ChinaTelecom
     6  *
     7  202.97.70.237  142.34 ms  *  China, ChinaTelecom
     8  *
     9  *
    10  *
    11  *
    12  111.24.2.105  169.61 ms  AS9808  China, ChinaMobile
    13  *
    14  *
    15  *
    16  211.136.67.166  171.70 ms  AS56048  China, Beijing, ChinaMobile
    17  211.136.95.226  173.07 ms  AS56048  China, Beijing, ChinaMobile
    18  *
    19  211.136.25.153  173.65 ms  AS56048  China, Beijing, ChinaMobile
    
    
    Traceroute to China, Shanghai CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.247.8.158 (58.247.8.158), 30 hops max, 32 byte packets
     1  154.17.0.1  27.09 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  7.22 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.21 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.184.157  127.69 ms  *  China, ChinaTelecom
     5  59.43.187.69  128.05 ms  *  China, ChinaTelecom
     6  59.43.130.209  128.55 ms  *  China, ChinaTelecom
     7  *
     8  219.158.9.97  157.54 ms  AS4837  China, ChinaUnicom
     9  139.226.227.42  155.07 ms  AS17621  China, Shanghai, ChinaUnicom
    10  139.226.228.46  150.26 ms  AS17621  China, Shanghai, ChinaUnicom
    11  139.226.225.22  158.24 ms  AS17621  China, Shanghai, ChinaUnicom
    12  58.247.8.153  161.10 ms  AS17621  China, Shanghai, ChinaUnicom
    13  *
    14  *
    15  *
    16  *
    17  *
    18  *
    19  *
    20  *
    21  *
    22  *
    23  *
    24  *
    25  *
    26  *
    27  *
    28  *
    29  *
    30  *
    
    
    Traceroute to China, Shanghai CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 180.153.28.5 (180.153.28.5), 30 hops max, 32 byte packets
     1  154.17.0.1  13.28 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.38 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.11 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.181.145  122.48 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.217  129.83 ms  *  China, ChinaTelecom
     7  101.95.88.18  134.00 ms  AS4812  China, Shanghai, ChinaTelecom
     8  *
     9  101.95.225.34  131.94 ms  AS4811  China, Shanghai, ChinaTelecom
    10  101.227.255.34  128.38 ms  AS4812  China, Shanghai, ChinaTelecom
    11  180.153.28.5  131.21 ms  AS4812  China, Shanghai, ChinaTelecom
    
    
    Traceroute to China, Shanghai CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 221.183.55.22 (221.183.55.22), 30 hops max, 32 byte packets
     1  154.17.0.1  4.60 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.29 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.15 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.181.145  122.52 ms  *  China, ChinaTelecom
     5  59.43.246.189  125.91 ms  *  China, ChinaTelecom
     6  *
     7  59.43.80.82  127.71 ms  *  China, ChinaTelecom
     8  *
     9  *
    10  221.183.86.102  164.46 ms  AS9808  China, ChinaMobile
    11  *
    12  221.176.17.178  237.98 ms  AS9808  China, ChinaMobile
    13  221.183.55.22  159.20 ms  AS9808  China, ChinaMobile
    
    
    Traceroute to China, Guangzhou CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.21.4.130 (210.21.4.130), 30 hops max, 32 byte packets
     1  154.17.0.1  2.87 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.39 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.12 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.184.117  148.11 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.145  151.19 ms  *  China, ChinaTelecom
     7  *
     8  219.158.10.249  155.13 ms  AS4837  China, ChinaUnicom
     9  112.92.0.62  255.33 ms  AS17816  China, Guangdong, Guangzhou, ChinaUnicom
    10  120.80.175.70  157.49 ms  AS17622  China, Guangdong, Guangzhou, ChinaUnicom
    11  *
    12  *
    13  *
    14  *
    15  *
    16  *
    17  *
    18  *
    19  *
    20  *
    21  *
    22  *
    23  *
    24  *
    25  *
    26  *
    27  *
    28  *
    29  *
    30  *
    
    
    Traceroute to China, Guangzhou CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 113.108.209.1 (113.108.209.1), 30 hops max, 32 byte packets
     1  154.17.0.1  10.78 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.38 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.22 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.184.117  148.13 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.105  162.72 ms  *  China, ChinaTelecom
     7  202.97.55.54  165.25 ms  AS4134  China, ChinaTelecom
     8  113.96.0.89  156.00 ms  AS58466  China, Guangdong, Guangzhou, ChinaTelecom
     9  113.108.209.1  164.42 ms  AS58466  China, Guangdong, Guangzhou, ChinaTelecom
    
    
    Traceroute to China, Guangzhou CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 120.196.212.25 (120.196.212.25), 30 hops max, 32 byte packets
     1  154.17.0.1  16.99 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.34 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.39 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.182.106  165.11 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.109  163.13 ms  *  China, ChinaTelecom
     7  202.97.55.174  166.15 ms  AS4134  China, ChinaTelecom
     8  *
     9  *
    10  221.176.22.185  172.66 ms  AS9808  China, ChinaMobile
    11  111.24.5.1  163.00 ms  AS9808  China, ChinaMobile
    12  111.24.5.222  182.10 ms  AS9808  China, ChinaMobile
    13  211.136.196.242  171.45 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    14  211.136.249.93  162.35 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    15  211.136.203.22  182.30 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    16  211.139.180.110  178.26 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    17  *
    18  *
    19  120.196.212.25  158.32 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    
    
    Traceroute to China, Shanghai CU AS9929 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.13.66.238 (210.13.66.238), 30 hops max, 32 byte packets
     1  154.17.0.1  4.80 ms  AS174,AS54574  United States, California, Los Angeles, cogentco.com
     2  193.41.248.225  0.44 ms  AS54574  United States, California, Los Angeles, dmit.io
     3  193.41.248.130  1.08 ms  AS54574  United States, California, Los Angeles, dmit.io
     4  59.43.184.157  127.66 ms  *  China, ChinaTelecom
     5  59.43.187.81  128.33 ms  *  China, ChinaTelecom
     6  59.43.130.213  130.16 ms  *  China, ChinaTelecom
     7  59.43.80.98  148.12 ms  *  China, ChinaTelecom
     8  *
     9  202.97.16.66  138.93 ms  AS4134  China, ChinaTelecom
    10  218.105.2.173  134.87 ms  AS9929  China, ChinaUnicom
    11  218.105.2.198  137.64 ms  AS9929  China, ChinaUnicom
    12  210.13.116.86  138.31 ms  AS9929  China, Shanghai, ChinaUnicom
    13  210.13.66.237  169.69 ms  AS9929  China, Shanghai, ChinaUnicom
    14  210.13.66.238  147.85 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Shanghai CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.32.0.1 (58.32.0.1), 30 hops max, 32 byte packets
     1  154.17.0.1  80.05 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.46 ms  Limit Exceeded! (frk@ipip.net)
     3  199.245.24.252  1.78 ms  Limit Exceeded! (frk@ipip.net)
     4  129.250.2.161  1.25 ms  Limit Exceeded! (frk@ipip.net)
     5  *
     6  129.250.6.129  111.64 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.2.59  106.43 ms  Limit Exceeded! (frk@ipip.net)
     8  117.103.177.106  103.68 ms  Limit Exceeded! (frk@ipip.net)
     9  59.43.184.181  132.04 ms  Limit Exceeded! (frk@ipip.net)
    10  59.43.187.57  137.19 ms  Limit Exceeded! (frk@ipip.net)
    11  59.43.138.65  141.05 ms  Limit Exceeded! (frk@ipip.net)
    12  61.152.24.186  172.51 ms  Limit Exceeded! (frk@ipip.net)
    13  58.32.0.1  142.32 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Guangzhou CT CN2 Gaming Broadband (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 119.121.0.1 (119.121.0.1), 30 hops max, 32 byte packets
     1  154.17.0.1  13.54 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.45 ms  Limit Exceeded! (frk@ipip.net)
     3  199.245.24.252  1.66 ms  Limit Exceeded! (frk@ipip.net)
     4  *
     5  *
     6  129.250.6.133  119.71 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.2.250  110.88 ms  Limit Exceeded! (frk@ipip.net)
     8  120.88.54.134  103.66 ms  Limit Exceeded! (frk@ipip.net)
     9  59.43.183.1  126.23 ms  Limit Exceeded! (frk@ipip.net)
    10  *
    11  59.43.138.53  149.08 ms  Limit Exceeded! (frk@ipip.net)
    12  59.43.17.205  135.06 ms  Limit Exceeded! (frk@ipip.net)
    13  *
    14  *
    15  119.121.0.1  169.53 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing Dr.Peng Home Network (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 14.131.128.1 (14.131.128.1), 30 hops max, 32 byte packets
     1  154.17.0.1  8.71 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.51 ms  Limit Exceeded! (frk@ipip.net)
     3  193.41.248.130  1.43 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.189.37  127.26 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.187.81  128.39 ms  Limit Exceeded! (frk@ipip.net)
     6  59.43.138.45  134.12 ms  Limit Exceeded! (frk@ipip.net)
     7  59.43.80.106  177.19 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  *
    10  *
    11  219.158.3.5  266.35 ms  Limit Exceeded! (frk@ipip.net)
    12  61.49.214.14  276.24 ms  Limit Exceeded! (frk@ipip.net)
    13  61.148.153.238  175.88 ms  Limit Exceeded! (frk@ipip.net)
    14  *
    15  *
    16  *
    17  *
    18  *
    19  *
    20  *
    21  *
    22  *
    23  *
    24  *
    25  *
    26  *
    27  *
    28  *
    29  *
    30  *
    
    
    Traceroute to China, Beijing Dr.Peng Network IDC Network (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.167.230.100 (211.167.230.100), 30 hops max, 32 byte packets
     1  154.17.0.1  3.23 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.39 ms  Limit Exceeded! (frk@ipip.net)
     3  193.41.248.130  1.28 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.189.37  127.29 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.187.69  127.90 ms  Limit Exceeded! (frk@ipip.net)
     6  59.43.138.49  132.28 ms  Limit Exceeded! (frk@ipip.net)
     7  59.43.80.145  133.42 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  *
    10  *
    11  219.158.3.1  171.66 ms  Limit Exceeded! (frk@ipip.net)
    12  61.49.214.26  173.78 ms  Limit Exceeded! (frk@ipip.net)
    13  202.96.13.238  165.45 ms  Limit Exceeded! (frk@ipip.net)
    14  61.51.37.206  173.72 ms  Limit Exceeded! (frk@ipip.net)
    15  218.241.244.14  175.14 ms  Limit Exceeded! (frk@ipip.net)
    16  218.241.252.14  199.15 ms  Limit Exceeded! (frk@ipip.net)
    17  218.241.253.214  170.89 ms  Limit Exceeded! (frk@ipip.net)
    18  218.241.245.54  181.31 ms  Limit Exceeded! (frk@ipip.net)
    19  *
    20  211.167.230.100  173.77 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CERNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.205.109.205 (202.205.109.205), 30 hops max, 32 byte packets
     1  154.17.0.1  14.86 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.38 ms  Limit Exceeded! (frk@ipip.net)
     3  193.41.248.130  1.12 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.184.117  148.12 ms  Limit Exceeded! (frk@ipip.net)
     5  *
     6  59.43.130.121  150.54 ms  Limit Exceeded! (frk@ipip.net)
     7  202.97.82.38  164.21 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  *
    10  *
    11  202.112.46.29  201.12 ms  Limit Exceeded! (frk@ipip.net)
    12  101.4.114.70  203.85 ms  Limit Exceeded! (frk@ipip.net)
    13  101.4.117.33  204.35 ms  Limit Exceeded! (frk@ipip.net)
    14  101.4.112.38  205.05 ms  Limit Exceeded! (frk@ipip.net)
    15  101.4.117.38  209.68 ms  Limit Exceeded! (frk@ipip.net)
    16  101.4.112.1  202.13 ms  Limit Exceeded! (frk@ipip.net)
    17  101.4.113.110  197.85 ms  Limit Exceeded! (frk@ipip.net)
    18  219.224.102.230  207.75 ms  Limit Exceeded! (frk@ipip.net)
    19  202.112.38.158  193.22 ms  Limit Exceeded! (frk@ipip.net)
    20  202.205.109.205  201.56 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CSTNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 159.226.254.1 (159.226.254.1), 30 hops max, 32 byte packets
     1  154.17.0.1  10.14 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.40 ms  Limit Exceeded! (frk@ipip.net)
     3  193.41.248.130  1.26 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.189.37  127.27 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.246.37  128.04 ms  Limit Exceeded! (frk@ipip.net)
     6  *
     7  63.218.211.65  180.47 ms  Limit Exceeded! (frk@ipip.net)
     8  63.218.210.74  182.57 ms  Limit Exceeded! (frk@ipip.net)
     9  63.217.16.34  159.18 ms  Limit Exceeded! (frk@ipip.net)
    10  159.226.254.61  194.21 ms  Limit Exceeded! (frk@ipip.net)
    11  159.226.254.61  194.35 ms  Limit Exceeded! (frk@ipip.net)
    12  159.226.253.121  178.22 ms  Limit Exceeded! (frk@ipip.net)
    13  159.226.254.1  201.64 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing GCable (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.156.140.17 (211.156.140.17), 30 hops max, 32 byte packets
     1  154.17.0.1  6.90 ms  Limit Exceeded! (frk@ipip.net)
     2  193.41.248.225  0.43 ms  Limit Exceeded! (frk@ipip.net)
     3  193.41.248.130  1.02 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.189.37  220.21 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.182.233  153.08 ms  Limit Exceeded! (frk@ipip.net)
     6  *
     7  59.43.132.17  154.29 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  106.120.252.154  151.42 ms  Limit Exceeded! (frk@ipip.net)
    10  60.247.93.254  155.50 ms  Limit Exceeded! (frk@ipip.net)
    11  211.156.128.198  154.23 ms  Limit Exceeded! (frk@ipip.net)
    12  211.156.128.85  155.53 ms  Limit Exceeded! (frk@ipip.net)
    13  211.156.140.17  155.41 ms  Limit Exceeded! (frk@ipip.net)
    
    
     -> Traceroute Test (IPV6)
    
    Traceroute to China, Beijing CU IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2408:80f0:4100:2005::3 (2408:80f0:4100:2005::3), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  240e:20:1800::cb:b658  131.25 ms  Limit Exceeded! (frk@ipip.net)
     6  240e:20:1800::112:f471  131.48 ms  Limit Exceeded! (frk@ipip.net)
     7  240e:0:a::c9:4a21  134.20 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  *
    10  *
    11  *
    12  2408:8000:2:8b0::  254.90 ms  Limit Exceeded! (frk@ipip.net)
    13  2408:8000:1100:338::3  254.95 ms  Limit Exceeded! (frk@ipip.net)
    14  2408:8000:1100:2413::3  253.38 ms  Limit Exceeded!
    15  2408:8000:1f10:3d03::3  263.53 ms  Limit Exceeded!
    16  2408:80f0:4100:2006::1  256.06 ms  Limit Exceeded!
    17  *
    18  *
    19  *
    20  *
    21  *
    22  *
    23  *
    24  *
    25  *
    26  *
    27  *
    28  *
    29  *
    30  *
    
    Traceroute to China, Shanghai CT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 240e:18:10:a01::1 (240e:18:10:a01::1), 30 hops max, 32 byte packets
     1  2605:52c0:2::1  5.51 ms  Limit Exceeded!
     2  2605:52c0::1000:1:1  0.40 ms  Limit Exceeded!
     3  2605:52c0::4809:4809  0.73 ms  Limit Exceeded!
     4  240e:20:1800::db:bd0c  1.15 ms  Limit Exceeded!
     5  240e:20:1800::cb:bd20  126.70 ms  Limit Exceeded!
     6  240e:20:1800::112:f475  131.90 ms  Limit Exceeded!
     7  *
     8  240e:0:a::c9:5385  129.08 ms  Limit Exceeded!
     9  240e:18:10:a01::1  130.56 ms  Limit Exceeded!
    
    Traceroute to China, Guangzhou CM IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2409:8057:5c00:30::6 (2409:8057:5c00:30::6), 30 hops max, 32 byte packets
     1  2605:52c0:2::1  1.81 ms  Limit Exceeded!
     2  2605:52c0::1000:1:1  0.35 ms  Limit Exceeded!
     3  2605:52c0::4809:4809  1.03 ms  Limit Exceeded!
     4  240e:20:1800::db:bd0c  1.21 ms  Limit Exceeded!
     5  240e:20:1800::cb:b650  127.95 ms  Limit Exceeded!
     6  240e:20:1800::112:f471  128.99 ms  Limit Exceeded!
     7  240e:0:a::c9:4a25  131.92 ms  Limit Exceeded!
     8  *
     9  *
    10  *
    11  *
    12  2409:8080:0:1:302:3e2::  366.55 ms  Limit Exceeded!
    13  2409:8080:1:2:302:302:3:0  286.64 ms  Limit Exceeded!
    14  2409:8080:1:2:302:376:0:1  288.76 ms  Limit Exceeded!
    15  2409:8055:0:140d::  293.80 ms  Limit Exceeded!
    16  *
    17  2409:8055:5c00:0:4c30::3  302.86 ms  Limit Exceeded!
    18  2409:8055:5c00:0:4c00::1  304.82 ms  Limit Exceeded!
    19  *
    20  *
    21  *
    22  2409:8057:5c00:30::6  302.70 ms  Limit Exceeded!
    
    Traceroute to China, Beijing CERNET2 IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:da8:a0:1001::1 (2001:da8:a0:1001::1), 30 hops max, 32 byte packets
     1  2605:52c0:2::1  3.68 ms  Limit Exceeded!
     2  2605:52c0::1000:1:1  0.46 ms  Limit Exceeded!
     3  2001:550:2:67::42:1  0.69 ms  Limit Exceeded!
     4  2001:550:0:1000::9a36:55e5  1.44 ms  Limit Exceeded!
     5  *
     6  *
     7  2001:550:2:18::22:2  6.37 ms  Limit Exceeded!
     8  2001:252:0:508::1  212.29 ms  Limit Exceeded!
     9  *
    10  *
    11  2001:252:0:1::1  259.67 ms  Limit Exceeded!
    12  2001:da8:a0:1001::1  296.52 ms  Limit Exceeded!
    
    Traceroute to China, Beijing CSTNET IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2400:dd00:0:37::213 (2400:dd00:0:37::213), 30 hops max, 32 byte packets
     1  2605:52c0:2::1  9.91 ms  Limit Exceeded!
     2  2605:52c0::1000:1:1  0.40 ms  Limit Exceeded!
     3  2001:550:2:67::42:1  0.71 ms  Limit Exceeded!
     4  2001:550:0:1000::9a36:55e5  1.41 ms  Limit Exceeded!
     5  *
     6  *
     7  2402:4480:2:3::1f:2  146.18 ms  Limit Exceeded!
     8  2400:dd00:0:40::195  181.13 ms  Limit Exceeded!
     9  2400:dd00:0:35::200  180.13 ms  Limit Exceeded!
    10  2400:dd00:0:37::213  185.27 ms  Limit Exceeded!

  [1]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/798672619.png
  [2]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2709543711.png
  [3]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2139142268.png
  [4]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/969158875.png
  [5]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/23178470.png
  [6]: https://cdn.jsdelivr.net/gh/qufengwu/blogstatic@latest/usr/uploads/2021/04/2139142268.png
