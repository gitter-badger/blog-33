---
title: Vultr洛杉矶VPS评测
date: 2021-06-01 04:21:37
tags:
- Vultr
- VPS
- 评测
categories: 商家评测
---

Vultr，美国知名主机商，按小时付费，有日本东京、新加坡、洛杉矶、硅谷等数据中心，国内线路不太行。CPU强悍，均在3GHz+；硬盘均为NVMe SSD，硬盘io非常好看。支持Paypal、支付宝付款。
<!--more-->

本文章发布时（2021-3-28），新用户注册并充值$10（≈￥65）可获得$100刀余额，赠送余额限期一个月。这似乎是个长期活动

## 相关索引 ##
官网地址（带AFF）:[https://www.vultr.com/?ref=8833279][1]
官网地址（无AFF）:[https://www.vultr.com][2]
测速地址（洛杉矶）：[http://lax-ca-us-ping.vultr.com/][3]
使用条款：[https://www.vultr.com/legal/tos/][4]



## 套餐详情 ##

 - 4x CPU核心
 - 16G 内存
 - 400G NVME SSD硬盘
 - 5000 Gb 流量
 - 1x 独立ipv4
 - 1x ipv6
 - KVM 虚拟化

## 测试详情 ##

### 系统信息 ###
 - CPU型号：Intel Core Processor (Skylake, IBRS)  3.70 GHz
 - CPU数量：4 vCPU
 - CPU缓存大小：16384 KB
 - 内存用量：746.42 MB / 15.66 GB
 - 无Swap内存
 - 硬盘用量：7.67 GB / 377.97 GB
 - 引导设备：/dev/vda1

### 网络信息 ###
 - IPV4 - ASN信息：20473 (AS-CHOOPA - Choopa, LLC, US)
 - IPV4 - 归属地：United States California Los Angeles
 - IPV6 - ASN信息：20473 (AS-CHOOPA - Choopa, LLC, US)
 - IPV6 - 归属地：United States United States 

### 流媒体解锁 ###
***全 都 不 支 持*** 

### CPU性能测试 (标准模式, 3-Pass @ 30sec) ###
 - 单线程测试：1307 Scores
 - 多线程测试：5182 Scores

### 内存性能测试 (标准模式, 3-Pass @ 30sec) ###
 - 单线程读：23859.57 MB/s
 - 单线程写：17641.11 MB/s

### 磁盘性能测试 (4K块/1M块, Direct写入) ###

| 测试项目       | 写速度                         | 读速度                        |
|----------------|--------------------------------|-------------------------------|
| 10MB-4K Block  | 99.9 MB/s (0.04 IOPS, 0.10 s)  | 113 MB/s (27496 IOPS, 0.09 s) |
| 10MB-1M Block  | 1.4 GB/s (1354 IOPS, 0.01 s)   | 898 MB/s (856 IOPS, 0.01 s)   |
| 100MB-4K Block | 97.4 MB/s (0.04 IOPS, 1.08 s)  | 119 MB/s (29082 IOPS, 0.88 s) |
| 100MB-1M Block | 1.1 GB/s (1055 IOPS, 0.09 s)   | 1.4 GB/s (1364 IOPS, 0.07 s)  |
| 1GB-4K Block   | 95.9 MB/s (0.04 IOPS, 10.93 s) | 121 MB/s (29440 IOPS, 8.70 s) |
| 1GB-1M Block   | 1.1 GB/s (1016 IOPS, 0.98 s)   | 1.3 GB/s (1281 IOPS, 0.78 s)  |

### Speedtest.net 网速测试 ###

网速在各个地区、各个运营商差别巨大，请谨慎购买
| 节点名称 | 上传速度     | 下载速度     | Ping      |
|----------|--------------|--------------|-----------|
| 最近节点 | 1059.12 MB/s | 1049.82 MB/s | 0.49 ms   |
| 南京联通 | 0.20 MB/s    | 17.58 MB/s   | 156.05 ms |
| 上海联通 | 40.47 MB/s   | 0.05 MB/s    | 178.96 ms |
| 杭州电信 | 1.66 MB/s    | 2.99 MB/s    | 174.74 ms |
| 南京电信 | 54.84 MB/s   | 534.31 MB/s  | 160.99 ms |
| 广州电信 | 7.57 MB/s    | 425.04 MB/s  | 168.13 ms |
| 沈阳移动 | 超时         | 超时         | 超时      |
| 南京移动 | 超时         | 超时         | 超时      |
| 南宁移动 | 37.53 MB/s   | 264.92 MB/s  | 221.63 ms |
| 兰州移动 | 40.27 MB/s   | 224.21 MB/s  | 237.98 ms |

### 路由追踪测试 ###


    Traceroute to China, Beijing CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 123.125.99.1 (123.125.99.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  6.27 ms  AS286,AS3257  United States, gtt.net
     6  62.115.119.40  0.77 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     7  199.229.231.206  2.36 ms  AS286,AS3257  GTT.NET BACKBONE, gtt.net
     8  219.158.96.233  171.49 ms  AS4837  China, ChinaUnicom
     9  219.158.98.17  166.87 ms  AS4837  China, ChinaUnicom
    10  219.158.3.181  169.35 ms  AS4837  China, ChinaUnicom
    11  219.158.8.85  201.39 ms  AS4837  China, ChinaUnicom
    12  *
    13  219.232.11.138  185.14 ms  AS4808  China, Beijing, ChinaUnicom
    14  61.148.158.106  186.07 ms  AS4808  China, Beijing, ChinaUnicom
    15  *
    16  *
    17  *
    18  123.125.99.1  205.37 ms  AS4808  China, Beijing, ChinaUnicom
    
    
    Traceroute to China, Beijing CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 180.149.128.1 (180.149.128.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.84 ms  AS286,AS3257  United States, gtt.net
     6  218.30.54.72  1.30 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     7  218.30.54.72  4.37 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     8  202.97.50.29  6.92 ms  AS4134  China, ChinaTelecom
     9  202.97.85.45  152.44 ms  AS4134  China, ChinaTelecom
    10  *
    11  *
    12  *
    13  180.149.128.1  174.31 ms  AS23724  China, Beijing, ChinaTelecom
    
    
    Traceroute to China, Beijing CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.136.25.153 (211.136.25.153), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  223.120.6.17  24.92 ms  AS58453  China, ChinaMobile
     7  223.120.6.17  25.22 ms  AS58453  China, ChinaMobile
     8  *
     9  *
    10  *
    11  *
    12  111.24.14.54  230.11 ms  AS9808  China, ChinaMobile
    13  111.24.14.46  220.22 ms  AS9808  China, ChinaMobile
    14  *
    15  211.136.95.226  224.78 ms  AS56048  China, Beijing, ChinaMobile
    16  *
    17  *
    18  *
    19  *
    20  211.136.25.153  215.13 ms  AS56048  China, Beijing, ChinaMobile
    
    
    Traceroute to China, Shanghai CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.247.0.49 (58.247.0.49), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  8.42 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     6  62.115.119.40  0.71 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     7  62.115.125.163  0.60 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     8  219.158.96.33  162.65 ms  AS4837  China, ChinaUnicom
     9  219.158.8.141  170.14 ms  AS4837  China, ChinaUnicom
    10  219.158.19.78  169.97 ms  AS4837  China, ChinaUnicom
    11  *
    12  *
    13  *
    14  58.247.0.49  222.05 ms  AS17621  China, Shanghai, ChinaUnicom
    
    
    Traceroute to China, Shanghai CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 180.153.28.1 (180.153.28.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  76.74.41.89  0.62 ms  AS286,AS3257  United States, gtt.net
     7  218.30.54.72  0.95 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     8  202.97.90.221  168.04 ms  AS4134  China, ChinaTelecom
     9  202.97.12.189  156.35 ms  AS4134  China, ChinaTelecom
    10  *
    11  61.152.24.9  160.61 ms  AS4812  China, Shanghai, ChinaTelecom
    12  *
    13  101.95.225.38  162.96 ms  AS4811  China, Shanghai, ChinaTelecom
    14  101.227.255.46  162.16 ms  AS4812  China, Shanghai, ChinaTelecom
    15  101.227.255.34  160.16 ms  AS4812  China, Shanghai, ChinaTelecom
    16  180.153.28.1  160.07 ms  AS4812  China, Shanghai, ChinaTelecom
    
    
    Traceroute to China, Shanghai CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 221.183.55.22 (221.183.55.22), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  223.120.6.17  24.85 ms  AS58453  China, ChinaMobile
     7  223.120.6.17  25.18 ms  AS58453  China, ChinaMobile
     8  *
     9  221.183.55.22  207.64 ms  AS9808  China, ChinaMobile
    
    
    Traceroute to China, Guangzhou CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.21.4.130 (210.21.4.130), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.78 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     6  89.149.180.26  7.73 ms  AS3257  Germany, gtt.net
     7  62.115.125.163  0.57 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     8  219.158.116.233  183.91 ms  AS4837  China, ChinaUnicom
     9  219.158.19.86  264.48 ms  AS4837  China, ChinaUnicom
    10  219.158.19.81  235.41 ms  AS4837  China, ChinaUnicom
    11  219.158.5.153  221.45 ms  AS4837  China, ChinaUnicom
    12  112.91.0.246  265.35 ms  AS17816  China, Guangdong, Guangzhou, ChinaUnicom
    13  112.91.0.246  239.09 ms  AS17816  China, Guangdong, Guangzhou, ChinaUnicom
    14  120.80.170.254  230.80 ms  AS17622  China, Guangdong, Guangzhou, ChinaUnicom
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
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.91 ms  AS286,AS3257  United States, gtt.net
     6  76.74.41.89  0.43 ms  AS286,AS3257  United States, gtt.net
     7  89.149.180.78  7.50 ms  AS3257  Germany, gtt.net
     8  202.97.50.77  13.61 ms  AS4134  China, ChinaTelecom
     9  202.97.50.77  11.51 ms  AS4134  China, ChinaTelecom
    10  202.97.12.26  159.56 ms  AS4134  China, ChinaTelecom
    11  202.97.94.133  175.72 ms  AS4134  China, ChinaTelecom
    12  113.96.0.97  169.05 ms  AS58466  China, Guangdong, Guangzhou, ChinaTelecom
    13  113.108.209.1  167.77 ms  AS58466  China, Guangdong, Guangzhou, ChinaTelecom
    
    
    Traceroute to China, Guangzhou CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.139.129.5 (211.139.129.5), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  *
     7  *
     8  223.120.32.5  178.41 ms  AS58453  China, ChinaMobile
     9  221.176.24.137  179.76 ms  AS9808  China, ChinaMobile
    10  221.176.18.109  167.38 ms  AS9808  China, ChinaMobile
    11  221.176.24.181  170.85 ms  AS9808  China, ChinaMobile
    12  111.24.14.141  160.86 ms  AS9808  China, ChinaMobile
    13  111.24.5.165  170.58 ms  AS9808  China, ChinaMobile
    14  211.136.208.193  171.52 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    15  211.139.129.5  174.44 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    
    
    Traceroute to China, Shanghai CU AS9929 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.13.66.238 (210.13.66.238), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  1.02 ms  AS286,AS3257  United States, gtt.net
     6  *
     7  144.232.17.60  7.52 ms  AS1239  United States, sprint.com
     8  144.232.0.152  3.54 ms  AS1239  United States, sprint.com
     9  144.232.17.60  7.76 ms  AS1239  United States, sprint.com
    10  144.232.17.29  14.84 ms  AS1239  United States, sprint.com
    11  218.105.2.198  145.04 ms  AS9929  China, ChinaUnicom
    12  144.232.22.215  10.58 ms  AS1239  United States, sprint.com
    13  144.223.242.10  167.40 ms  AS1239  United States, California, San Jose, sprint.com
    14  218.105.2.198  170.28 ms  AS9929  China, ChinaUnicom
    15  *
    16  210.13.66.238  150.21 ms  AS9929  China, Shanghai, ChinaUnicom
    
    
    Traceroute to China, Shanghai CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.32.0.1 (58.32.0.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.36 ms  AS2914  United States, ntt.com
     6  *
     7  129.250.3.192  108.79 ms  AS2914  United States, ntt.com
     8  129.250.6.129  109.93 ms  AS2914  United States, ntt.com
     9  129.250.2.69  108.49 ms  AS2914  United States, ntt.com
    10  59.43.187.73  133.11 ms  *  China, ChinaTelecom
    11  59.43.247.114  140.03 ms  *  China, ChinaTelecom
    12  61.152.24.190  140.54 ms  AS4812  China, Shanghai, ChinaTelecom
    13  *
    14  61.152.24.190  162.22 ms  AS4812  China, Shanghai, ChinaTelecom
    15  58.32.0.1  145.95 ms  AS4812  China, Shanghai, ChinaTelecom
    
    
    Traceroute to China, Guangzhou CT CN2 Gaming Broadband (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 119.121.0.1 (119.121.0.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  3.83 ms  AS2914  United States, ntt.com
     6  129.250.2.117  2.55 ms  AS2914  United States, ntt.com
     7  129.250.3.192  108.70 ms  AS2914  United States, ntt.com
     8  129.250.6.133  118.13 ms  AS2914  United States, ntt.com
     9  129.250.2.69  114.97 ms  AS2914  United States, ntt.com
    10  *
    11  59.43.130.109  165.92 ms  *  China, ChinaTelecom
    12  *
    13  119.121.0.1  157.82 ms  AS134773  China, Guangdong, Guangzhou, ChinaTelecom
    
    
    Traceroute to China, Beijing Dr.Peng Home Network (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 14.131.128.1 (14.131.128.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  3.39 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     6  89.149.130.90  0.55 ms  AS3257  United States, California, Los Angeles, gtt.net
     7  62.115.125.163  1.88 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     8  219.158.34.249  18.77 ms  AS4837  China, ChinaUnicom
     9  219.158.96.210  170.97 ms  AS4837  China, ChinaUnicom
    10  219.158.3.141  158.69 ms  AS4837  China, ChinaUnicom
    11  219.158.112.25  224.35 ms  AS4837  China, ChinaUnicom
    12  202.96.12.2  220.94 ms  AS4808  China, Beijing, ChinaUnicom
    13  202.96.13.222  223.67 ms  AS4808  China, Beijing, ChinaUnicom
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
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.41 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     6  62.115.119.40  0.82 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     7  173.241.128.46  1.14 ms  AS286,AS3257  United States, gtt.net
     8  62.115.154.91  18.93 ms  AS1299  Sweden, Stockholm County, Stockholm, telia.com
     9  219.158.96.25  164.67 ms  AS4837  China, ChinaUnicom
    10  *
    11  219.158.4.173  231.45 ms  Limit Exceeded! (frk@ipip.net)
    12  125.33.186.18  223.28 ms  Limit Exceeded! (frk@ipip.net)
    13  202.96.13.214  214.56 ms  Limit Exceeded! (frk@ipip.net)
    14  *
    15  218.241.244.2  216.65 ms  Limit Exceeded! (frk@ipip.net)
    16  218.241.255.86  221.50 ms  Limit Exceeded! (frk@ipip.net)
    17  218.241.253.130  214.86 ms  Limit Exceeded! (frk@ipip.net)
    18  211.167.230.100  220.06 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CERNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.205.109.205 (202.205.109.205), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  1.09 ms  Limit Exceeded! (frk@ipip.net)
     6  129.250.2.161  1.50 ms  Limit Exceeded! (frk@ipip.net)
     7  *
     8  129.250.5.23  115.88 ms  Limit Exceeded! (frk@ipip.net)
     9  *
    10  129.250.6.123  162.20 ms  Limit Exceeded! (frk@ipip.net)
    11  203.131.254.214  156.86 ms  Limit Exceeded! (frk@ipip.net)
    12  101.4.114.181  192.82 ms  Limit Exceeded! (frk@ipip.net)
    13  101.4.118.121  245.54 ms  Limit Exceeded! (frk@ipip.net)
    14  101.4.117.253  285.95 ms  Limit Exceeded! (frk@ipip.net)
    15  101.4.116.205  260.84 ms  Limit Exceeded! (frk@ipip.net)
    16  219.224.102.230  257.64 ms  Limit Exceeded! (frk@ipip.net)
    17  202.112.38.158  265.82 ms  Limit Exceeded! (frk@ipip.net)
    18  202.205.109.205  276.09 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CSTNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 159.226.254.1 (159.226.254.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.35 ms  Limit Exceeded! (frk@ipip.net)
     6  129.250.2.17  1.49 ms  Limit Exceeded! (frk@ipip.net)
     7  *
     8  154.54.42.101  0.93 ms  Limit Exceeded! (frk@ipip.net)
     9  63.223.17.94  157.92 ms  Limit Exceeded! (frk@ipip.net)
    10  154.18.4.2  152.91 ms  Limit Exceeded! (frk@ipip.net)
    11  159.226.254.61  198.94 ms  Limit Exceeded! (frk@ipip.net)
    12  159.226.254.1  193.12 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing GCable (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.156.140.17 (211.156.140.17), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  76.74.41.89  4.64 ms  Limit Exceeded! (frk@ipip.net)
     7  202.97.83.229  9.71 ms  Limit Exceeded! (frk@ipip.net)
     8  202.97.83.229  1.19 ms  Limit Exceeded! (frk@ipip.net)
     9  202.97.41.197  153.59 ms  Limit Exceeded! (frk@ipip.net)
    10  *
    11  *
    12  *
    13  *
    14  60.247.93.254  152.04 ms  Limit Exceeded! (frk@ipip.net)
    15  *
    16  211.156.128.85  154.90 ms  Limit Exceeded! (frk@ipip.net)
    17  211.156.128.85  154.77 ms  Limit Exceeded! (frk@ipip.net)
    18  *
    19  211.156.140.17  155.58 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.160.95.218 (203.160.95.218), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  0.77 ms  Limit Exceeded! (frk@ipip.net)
     6  129.250.2.161  0.67 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.3.192  109.90 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  129.250.2.51  163.46 ms  Limit Exceeded! (frk@ipip.net)
    10  129.250.6.121  158.26 ms  Limit Exceeded! (frk@ipip.net)
    11  203.160.95.218  164.27 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.215.232.173 (203.215.232.173), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  76.74.41.89  0.64 ms  Limit Exceeded! (frk@ipip.net)
     7  218.30.54.72  2.16 ms  Limit Exceeded! (frk@ipip.net)
     8  202.97.92.46  2.51 ms  Limit Exceeded! (frk@ipip.net)
     9  *
    10  *
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
    
    
    Traceroute to China, Hongkong CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.8.25.187 (203.8.25.187), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.34 ms  Limit Exceeded! (frk@ipip.net)
     6  *
     7  129.250.3.192  104.20 ms  Limit Exceeded! (frk@ipip.net)
     8  213.248.79.253  1.20 ms  Limit Exceeded! (frk@ipip.net)
     9  129.250.2.69  109.02 ms  Limit Exceeded! (frk@ipip.net)
    10  117.103.177.106  115.77 ms  Limit Exceeded! (frk@ipip.net)
    11  59.43.184.197  158.22 ms  Limit Exceeded! (frk@ipip.net)
    12  59.43.248.146  164.80 ms  Limit Exceeded! (frk@ipip.net)
    13  203.8.25.187  171.41 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.142.105.9 (203.142.105.9), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  *
     7  223.120.6.17  25.00 ms  Limit Exceeded! (frk@ipip.net)
     8  223.120.32.5  177.93 ms  Limit Exceeded! (frk@ipip.net)
     9  *
    10  223.119.17.1  179.95 ms  Limit Exceeded! (frk@ipip.net)
    11  203.142.126.6  180.12 ms  Limit Exceeded! (frk@ipip.net)
    12  203.142.126.6  179.98 ms  Limit Exceeded! (frk@ipip.net)
    13  203.142.100.22  180.73 ms  Limit Exceeded! (frk@ipip.net)
    14  203.142.105.9  180.51 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong HGC (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 218.188.104.30 (218.188.104.30), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.35 ms  Limit Exceeded! (frk@ipip.net)
     6  129.250.2.117  0.74 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.3.192  110.90 ms  Limit Exceeded! (frk@ipip.net)
     8  129.250.5.23  109.05 ms  Limit Exceeded! (frk@ipip.net)
     9  129.250.2.51  162.79 ms  Limit Exceeded! (frk@ipip.net)
    10  129.250.6.123  167.05 ms  Limit Exceeded! (frk@ipip.net)
    11  203.131.245.46  150.93 ms  Limit Exceeded! (frk@ipip.net)
    12  218.189.5.56  150.42 ms  Limit Exceeded! (frk@ipip.net)
    13  218.188.104.30  164.18 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong HKBN (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.6.23.239 (210.6.23.239), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  206.72.210.194  191.63 ms  Limit Exceeded! (frk@ipip.net)
     7  203.186.235.137  205.38 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  210.6.23.239  165.72 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong PCCW (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.85.125.60 (202.85.125.60), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  0.28 ms  Limit Exceeded! (frk@ipip.net)
     6  129.250.2.105  1.29 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.3.17  1.14 ms  Limit Exceeded! (frk@ipip.net)
     8  129.250.8.102  0.86 ms  Limit Exceeded! (frk@ipip.net)
     9  63.223.20.33  150.56 ms  Limit Exceeded! (frk@ipip.net)
    10  63.222.45.38  150.04 ms  Limit Exceeded! (frk@ipip.net)
    11  202.153.99.204  154.18 ms  Limit Exceeded! (frk@ipip.net)
    12  202.153.99.203  165.75 ms  Limit Exceeded! (frk@ipip.net)
    13  203.215.244.33  160.00 ms  Limit Exceeded! (frk@ipip.net)
    14  202.85.125.60  156.02 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong TGT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.123.76.239 (202.123.76.239), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.36 ms  Limit Exceeded! (frk@ipip.net)
     6  89.149.186.245  169.27 ms  Limit Exceeded! (frk@ipip.net)
     7  129.250.3.192  109.67 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  203.78.73.75  160.46 ms  Limit Exceeded! (frk@ipip.net)
    10  *
    11  203.131.254.14  150.22 ms  Limit Exceeded! (frk@ipip.net)
    12  203.78.72.100  159.41 ms  Limit Exceeded! (frk@ipip.net)
    13  203.78.73.75  159.34 ms  Limit Exceeded! (frk@ipip.net)
    14  202.123.76.239  160.88 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Hongkong WTT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 59.152.252.242 (59.152.252.242), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  206.72.210.200  161.05 ms  Limit Exceeded!
     6  206.72.210.200  159.92 ms  Limit Exceeded!
     7  115.160.187.54  160.32 ms  Limit Exceeded!
     8  *
     9  59.152.252.196  160.46 ms  Limit Exceeded!
    10  59.152.252.242  160.48 ms  Limit Exceeded!
    
    
    Traceroute to Singapore, China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.215.233.1 (203.215.233.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  6.32 ms  Limit Exceeded!
     6  218.30.54.72  3.47 ms  Limit Exceeded!
     7  218.30.54.72  7.72 ms  Limit Exceeded!
     8  202.97.50.21  0.67 ms  Limit Exceeded!
     9  202.97.51.101  153.07 ms  Limit Exceeded!
    10  203.215.233.1  252.56 ms  Limit Exceeded!
    
    
    Traceroute to Singapore, China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 183.91.61.1 (183.91.61.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  20.89 ms  Limit Exceeded!
     6  129.250.2.161  3.81 ms  Limit Exceeded!
     7  129.250.3.192  117.15 ms  Limit Exceeded!
     8  129.250.6.133  104.95 ms  Limit Exceeded!
     9  129.250.2.250  119.91 ms  Limit Exceeded!
    10  117.103.177.106  107.86 ms  Limit Exceeded!
    11  183.91.61.1  191.69 ms  Limit Exceeded!
    
    
    Traceroute to Singapore, Singtel (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 118.201.1.11 (118.201.1.11), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.41 ms  Limit Exceeded!
     6  62.115.149.36  0.56 ms  Limit Exceeded!
     7  62.115.119.40  1.11 ms  Limit Exceeded!
     8  62.115.8.203  0.61 ms  Limit Exceeded!
     9  203.208.182.77  204.02 ms  Limit Exceeded!
    10  203.208.172.145  178.30 ms  Limit Exceeded!
    11  203.208.177.214  179.89 ms  Limit Exceeded!
    12  203.208.177.214  180.04 ms  Limit Exceeded!
    13  203.208.177.214  170.55 ms  Limit Exceeded!
    14  203.208.177.214  179.11 ms  Limit Exceeded!
    15  *
    16  203.125.232.130  180.68 ms  Limit Exceeded!
    17  203.125.232.130  180.71 ms  Limit Exceeded!
    18  165.21.49.126  168.61 ms  Limit Exceeded!
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
    
    
    Traceroute to Singapore, StarHub (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.116.46.33 (203.116.46.33), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.56 ms  Limit Exceeded!
     6  62.115.119.129  0.79 ms  Limit Exceeded!
     7  129.250.3.192  109.72 ms  Limit Exceeded!
     8  129.250.2.66  185.36 ms  Limit Exceeded!
     9  129.250.4.94  184.88 ms  Limit Exceeded!
    10  116.51.18.138  248.47 ms  Limit Exceeded!
    11  61.8.243.1  196.20 ms  Limit Exceeded!
    12  61.8.243.1  181.51 ms  Limit Exceeded!
    13  203.116.46.33  197.25 ms  Limit Exceeded!
    
    
    Traceroute to Singapore, M1 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 118.189.184.1 (118.189.184.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.50 ms  Limit Exceeded!
     6  62.115.149.36  0.53 ms  Limit Exceeded!
     7  62.115.125.163  4.79 ms  Limit Exceeded!
     8  62.115.125.163  3.83 ms  Limit Exceeded!
     9  202.65.246.14  352.52 ms  Limit Exceeded!
    10  202.65.246.137  382.59 ms  Limit Exceeded!
    11  202.65.246.137  374.58 ms  Limit Exceeded!
    12  202.65.246.186  387.52 ms  Limit Exceeded!
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
    
    
    Traceroute to Singapore, M1 GamePro (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 118.189.38.17 (118.189.38.17), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  62.115.119.129  0.99 ms  Limit Exceeded!
     7  62.115.134.42  195.13 ms  Limit Exceeded!
     8  62.115.134.42  195.43 ms  Limit Exceeded!
     9  62.115.57.135  195.51 ms  Limit Exceeded!
    10  203.211.159.149  196.56 ms  Limit Exceeded!
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
    
    
    Traceroute to Singapore, AWS (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 13.228.0.251 (13.228.0.251), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  1.53 ms  Limit Exceeded!
     6  129.250.2.105  1.46 ms  Limit Exceeded!
     7  129.250.3.192  109.72 ms  Limit Exceeded!
     8  129.250.2.66  183.96 ms  Limit Exceeded!
     9  129.250.2.97  393.01 ms  Limit Exceeded!
    10  116.51.17.26  391.78 ms  Limit Exceeded!
    11  150.222.3.63  165.87 ms  Limit Exceeded!
    12  52.93.11.83  396.49 ms  Limit Exceeded!
    13  *
    14  150.222.108.185  390.07 ms  Limit Exceeded!
    15  203.83.223.15  401.26 ms  Limit Exceeded!
    16  *
    17  *
    18  *
    19  *
    20  *
    21  *
    22  13.228.0.251  395.74 ms  Limit Exceeded!
    
    
    Traceroute to Japan, NTT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 61.213.155.84 (61.213.155.84), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.48 ms  Limit Exceeded!
     6  129.250.2.117  1.07 ms  Limit Exceeded!
     7  129.250.3.192  109.96 ms  Limit Exceeded!
     8  129.250.3.28  117.21 ms  Limit Exceeded!
     9  61.213.179.34  113.39 ms  Limit Exceeded!
    10  *
    11  *
    12  61.213.155.84  126.89 ms  Limit Exceeded!
    
    
    Traceroute to Japan, IIJ (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.232.15.70 (202.232.15.70), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.38 ms  Limit Exceeded!
     6  *
     7  129.250.2.114  18.53 ms  Limit Exceeded!
     8  168.143.229.26  0.53 ms  Limit Exceeded!
     9  58.138.88.157  116.85 ms  Limit Exceeded!
    10  58.138.102.210  108.97 ms  Limit Exceeded!
    11  210.130.142.114  117.33 ms  Limit Exceeded!
    12  202.232.15.70  109.71 ms  Limit Exceeded!
    
    
    Traceroute to Japan, SoftBank (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.175.32.26 (210.175.32.26), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  206.72.211.18  1.03 ms  Limit Exceeded!
     6  *
     7  143.90.232.241  101.37 ms  Limit Exceeded!
     8  143.90.232.241  103.12 ms  Limit Exceeded!
     9  143.90.26.226  101.29 ms  Limit Exceeded!
    10  143.90.54.30  102.10 ms  Limit Exceeded!
    11  210.175.32.123  102.39 ms  Limit Exceeded!
    12  210.175.32.26  102.40 ms  Limit Exceeded!
    
    
    Traceroute to Japan, KDDI (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 106.162.242.108 (106.162.242.108), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  76.74.41.89  0.46 ms  Limit Exceeded!
     7  208.116.133.198  0.44 ms  Limit Exceeded!
     8  203.181.106.189  0.53 ms  Limit Exceeded!
     9  106.187.12.1  104.14 ms  Limit Exceeded!
    10  111.107.101.94  107.37 ms  Limit Exceeded!
    11  111.107.101.94  102.83 ms  Limit Exceeded!
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
    
    
    Traceroute to Japan, China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.215.236.3 (203.215.236.3), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.32 ms  Limit Exceeded!
     6  76.74.41.89  6.75 ms  Limit Exceeded!
     7  202.97.92.38  3.94 ms  Limit Exceeded!
     8  202.97.92.38  1.68 ms  Limit Exceeded!
     9  203.215.236.3  114.69 ms  Limit Exceeded!
    
    
    Traceroute to Japan, China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.55.27.4 (202.55.27.4), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  4.82 ms  Limit Exceeded!
     6  *
     7  129.250.3.192  109.94 ms  Limit Exceeded!
     8  213.248.79.253  1.18 ms  Limit Exceeded!
     9  *
    10  117.103.177.106  107.79 ms  Limit Exceeded!
    11  202.55.27.4  106.43 ms  Limit Exceeded!
    
    
    Traceroute to Japan, Amazon AWS (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 13.112.63.251 (13.112.63.251), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  6.06 ms  Limit Exceeded!
     6  129.250.2.117  0.99 ms  Limit Exceeded!
     7  129.250.3.192  103.80 ms  Limit Exceeded!
     8  129.250.7.33  105.38 ms  Limit Exceeded!
     9  61.120.146.70  124.52 ms  Limit Exceeded!
    10  54.239.53.246  109.95 ms  Limit Exceeded!
    11  150.222.91.37  108.87 ms  Limit Exceeded!
    12  *
    13  *
    14  *
    15  52.95.31.43  111.02 ms  Limit Exceeded!
    16  52.93.73.244  130.35 ms  Limit Exceeded!
    17  52.95.31.198  112.25 ms  Limit Exceeded!
    18  52.95.31.102  111.61 ms  Limit Exceeded!
    19  52.93.250.36  111.48 ms  Limit Exceeded!
    20  *
    21  *
    22  *
    23  *
    24  *
    25  *
    26  13.112.63.251  115.70 ms  Limit Exceeded!
    
    
    Traceroute to South Korea, KT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.114.41.101 (210.114.41.101), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  89.149.187.114  4.52 ms  Limit Exceeded!
     7  89.149.187.114  1.35 ms  Limit Exceeded!
     8  *
     9  112.174.88.217  619.19 ms  Limit Exceeded!
    10  *
    11  112.174.60.250  140.20 ms  Limit Exceeded!
    12  112.188.247.210  157.67 ms  Limit Exceeded!
    13  220.90.203.6  158.21 ms  Limit Exceeded!
    14  220.90.203.6  164.30 ms  Limit Exceeded!
    15  210.114.41.101  157.93 ms  Limit Exceeded!
    
    
    Traceroute to South Korea, SK (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 175.122.253.62 (175.122.253.62), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  206.72.210.167  0.67 ms  Limit Exceeded!
     6  58.229.4.172  136.66 ms  Limit Exceeded!
     7  58.229.12.66  136.95 ms  Limit Exceeded!
     8  *
     9  *
    10  *
    11  175.122.253.62  136.80 ms  Limit Exceeded!
    
    
    Traceroute to South Korea, LG (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.174.62.44 (211.174.62.44), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.50 ms  Limit Exceeded!
     6  62.115.119.129  0.90 ms  Limit Exceeded!
     7  64.86.197.98  1.01 ms  Limit Exceeded!
     8  62.115.125.161  6.83 ms  Limit Exceeded!
     9  206.82.129.18  1.84 ms  Limit Exceeded!
    10  144.232.15.244  14.50 ms  Limit Exceeded!
    11  1.213.105.145  0.55 ms  Limit Exceeded!
    12  144.223.179.178  32.28 ms  Limit Exceeded!
    13  1.213.104.221  10.74 ms  Limit Exceeded!
    14  203.255.234.181  141.09 ms  Limit Exceeded!
    15  *
    16  *
    17  *
    18  *
    19  *
    20  *
    21  211.174.62.44  141.80 ms  Limit Exceeded!
    
    
    Traceroute to South Korea, China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 218.185.246.3 (218.185.246.3), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  1.32 ms  Limit Exceeded!
     6  *
     7  129.250.3.192  109.81 ms  Limit Exceeded!
     8  129.250.6.129  110.60 ms  Limit Exceeded!
     9  129.250.2.59  98.55 ms  Limit Exceeded!
    10  117.103.177.106  116.27 ms  Limit Exceeded!
    11  *
    12  59.43.246.37  141.22 ms  Limit Exceeded!
    13  218.185.246.3  163.66 ms  Limit Exceeded!
    
    
    Traceroute to South Korea, Amazon AWS (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 13.124.63.251 (13.124.63.251), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  1.24 ms  Limit Exceeded!
     6  129.250.2.17  1.79 ms  Limit Exceeded!
     7  129.250.2.177  104.21 ms  Limit Exceeded!
     8  129.250.6.133  117.94 ms  Limit Exceeded!
     9  61.120.146.118  117.72 ms  Limit Exceeded!
    10  *
    11  *
    12  54.239.53.163  104.94 ms  Limit Exceeded!
    13  52.93.66.113  119.53 ms  Limit Exceeded!
    14  *
    15  *
    16  *
    17  52.93.248.142  140.12 ms  Limit Exceeded!
    18  52.93.248.193  131.11 ms  Limit Exceeded!
    19  54.239.123.141  143.75 ms  Limit Exceeded!
    20  54.239.122.28  139.84 ms  Limit Exceeded!
    21  54.239.122.67  148.77 ms  Limit Exceeded!
    22  54.239.122.28  137.03 ms  Limit Exceeded!
    23  *
    24  *
    25  *
    26  *
    27  13.124.63.251  130.15 ms  Limit Exceeded!
    
    
    Traceroute to China, Taiwan Chief (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.133.242.116 (202.133.242.116), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  206.72.210.108  7.79 ms  Limit Exceeded!
     7  175.41.58.41  10.27 ms  Limit Exceeded!
     8  175.41.61.169  128.61 ms  Limit Exceeded!
     9  *
    10  *
    11  *
    12  *
    13  *
    14  202.133.242.116  148.82 ms  Limit Exceeded!
    
    
    Traceroute to China, Taiwan APTG (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.200.69.90 (210.200.69.90), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  203.78.181.205  8.38 ms  Limit Exceeded!
     7  175.41.61.169  138.68 ms  Limit Exceeded!
     8  175.41.61.169  141.01 ms  Limit Exceeded!
     9  203.78.181.134  132.47 ms  Limit Exceeded!
    10  203.79.253.161  157.14 ms  Limit Exceeded!
    11  210.200.80.254  157.52 ms  Limit Exceeded!
    12  210.200.80.254  157.71 ms  Limit Exceeded!
    13  210.200.80.254  153.75 ms  Limit Exceeded!
    14  210.200.69.90  160.89 ms  Limit Exceeded!
    
    
    Traceroute to China, Taiwan CHT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 203.75.129.162 (203.75.129.162), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  62.115.149.36  0.43 ms  Limit Exceeded!
     7  62.115.162.87  0.67 ms  Limit Exceeded!
     8  202.39.91.54  141.86 ms  Limit Exceeded!
     9  202.39.91.54  141.77 ms  Limit Exceeded!
    10  *
    11  *
    12  211.22.229.45  135.01 ms  Limit Exceeded!
    13  1.1.1.2  139.35 ms  Limit Exceeded!
    14  1.1.1.2  139.59 ms  Limit Exceeded!
    15  *
    16  203.75.129.162  140.31 ms  Limit Exceeded!
    
    
    Traceroute to China, Taiwan TFN (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 219.87.66.3 (219.87.66.3), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  2.34 ms  Limit Exceeded!
     6  *
     7  *
     8  129.250.7.6  139.82 ms  Limit Exceeded!
     9  129.250.7.41  134.94 ms  Limit Exceeded!
    10  61.58.33.222  142.09 ms  Limit Exceeded!
    11  60.199.14.246  132.86 ms  Limit Exceeded!
    12  60.199.16.62  139.02 ms  Limit Exceeded!
    13  219.87.66.3  128.52 ms  Limit Exceeded!
    
    
    Traceroute to China,Taiwan FET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.73.144.38 (211.73.144.38), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.42 ms  Limit Exceeded!
     6  89.149.140.77  16.57 ms  Limit Exceeded!
     7  62.115.162.135  17.90 ms  Limit Exceeded!
     8  202.84.253.85  2.50 ms  Limit Exceeded!
     9  129.250.7.112  146.76 ms  Limit Exceeded!
    10  202.84.140.225  106.09 ms  Limit Exceeded!
    11  199.245.16.34  140.42 ms  Limit Exceeded!
    12  192.72.155.113  134.03 ms  Limit Exceeded!
    13  202.84.137.250  164.34 ms  Limit Exceeded!
    14  *
    15  *
    16  *
    17  211.73.144.38  140.64 ms  Limit Exceeded!
    
    
    Traceroute to China, Taiwan KBT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 61.63.0.102 (61.63.0.102), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.81 ms  Limit Exceeded!
     6  62.115.119.129  0.85 ms  Limit Exceeded!
     7  129.250.3.238  2.66 ms  Limit Exceeded!
     8  129.250.8.102  1.05 ms  Limit Exceeded!
     9  203.78.181.201  140.01 ms  Limit Exceeded!
    10  63.223.9.234  129.46 ms  Limit Exceeded!
    11  203.187.3.25  137.50 ms  Limit Exceeded!
    12  203.187.3.25  133.46 ms  Limit Exceeded!
    13  203.187.9.226  129.95 ms  Limit Exceeded!
    14  61.63.63.6  130.31 ms  Limit Exceeded!
    15  61.63.0.123  134.30 ms  Limit Exceeded!
    16  58.86.0.206  145.10 ms  Limit Exceeded!
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
    
    
    Traceroute to China, Taiwan TAIFO (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 103.31.196.203 (103.31.196.203), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  206.72.210.122  0.68 ms  Limit Exceeded!
     6  206.72.210.122  0.59 ms  Limit Exceeded!
     7  184.105.64.6  137.56 ms  Limit Exceeded!
     8  184.105.64.6  137.31 ms  Limit Exceeded!
     9  *
    10  113.21.95.123  136.22 ms  Limit Exceeded!
    11  113.21.95.123  138.40 ms  Limit Exceeded!
    12  *
    13  103.31.197.122  138.50 ms  Limit Exceeded!
    14  103.31.197.70  136.74 ms  Limit Exceeded!
    15  103.31.197.70  136.67 ms  Limit Exceeded!
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
    
    
    Traceroute to United States, Los Angeles China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 218.30.33.17 (218.30.33.17), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  1.33 ms  Limit Exceeded!
     6  218.30.54.72  3.26 ms  Limit Exceeded!
     7  218.30.54.72  6.37 ms  Limit Exceeded!
     8  202.97.50.25  6.75 ms  Limit Exceeded!
     9  218.30.33.17  54.35 ms  Limit Exceeded!
    
    
    Traceroute to United States, Los Angeles China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 66.102.252.100 (66.102.252.100), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  66.102.252.100  0.70 ms  Limit Exceeded!
    
    
    Traceroute to United States, Los Angeles PCCW (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 63.218.42.81 (63.218.42.81), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  1.76 ms  Limit Exceeded!
     6  *
     7  62.115.125.163  0.52 ms  Limit Exceeded!
     8  *
     9  *
    10  63.218.42.81  0.84 ms  Limit Exceeded!
    
    
    Traceroute to United States, Los Angeles HE (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 66.220.18.42 (66.220.18.42), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  72.52.92.121  0.64 ms  Limit Exceeded!
     7  72.52.92.121  0.65 ms  Limit Exceeded!
     8  66.220.18.42  0.64 ms  Limit Exceeded!
    
    
    Traceroute to United States, Los Angeles GTT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 173.205.77.98 (173.205.77.98), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.45 ms  Limit Exceeded!
     6  *
     7  129.250.3.178  2.50 ms  Limit Exceeded!
     8  140.174.28.58  0.81 ms  Limit Exceeded!
     9  23.203.155.191  17.56 ms  Limit Exceeded!
    10  *
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
    
    
    Traceroute to United States, San Fransico ATT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 12.169.215.33 (12.169.215.33), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.52 ms  Limit Exceeded!
     6  89.149.140.77  24.08 ms  Limit Exceeded!
     7  129.250.2.114  2.52 ms  Limit Exceeded!
     8  129.250.9.62  2.11 ms  Limit Exceeded!
     9  12.122.18.10  16.22 ms  Limit Exceeded!
    10  12.122.28.122  18.30 ms  Limit Exceeded!
    11  12.244.156.30  17.31 ms  Limit Exceeded!
    12  12.244.156.30  14.26 ms  Limit Exceeded!
    13  12.169.215.33  13.05 ms  Limit Exceeded!
    
    
    Traceroute to United States, New York TATA (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 66.198.181.100 (66.198.181.100), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.43 ms  Limit Exceeded!
     6  62.115.119.40  0.98 ms  Limit Exceeded!
     7  129.250.3.123  1.03 ms  Limit Exceeded!
     8  63.243.250.58  72.64 ms  Limit Exceeded!
     9  *
    10  63.243.205.72  70.06 ms  Limit Exceeded!
    11  64.86.62.25  66.37 ms  Limit Exceeded!
    12  64.86.62.25  66.49 ms  Limit Exceeded!
    13  209.58.75.217  66.49 ms  Limit Exceeded!
    14  209.58.75.198  66.13 ms  Limit Exceeded!
    15  *
    16  66.198.181.100  66.34 ms  Limit Exceeded!
    
    
    Traceroute to United States, San Jose China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 218.30.33.17 (218.30.33.17), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  3.48 ms  Limit Exceeded!
     6  76.74.41.89  0.43 ms  Limit Exceeded!
     7  218.30.54.72  1.38 ms  Limit Exceeded!
     8  202.97.50.25  2.75 ms  Limit Exceeded!
     9  218.30.33.17  61.00 ms  Limit Exceeded!
    
    
    Traceroute to United States, San Jose NTT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 23.11.26.62 (23.11.26.62), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  1.33 ms  Limit Exceeded!
     6  *
     7  129.250.4.150  11.59 ms  Limit Exceeded!
     8  129.250.2.48  7.76 ms  Limit Exceeded!
     9  23.11.26.62  8.10 ms  Limit Exceeded!
    
    
    Traceroute to United States, Fremont HE (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 72.52.104.74 (72.52.104.74), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  206.72.210.122  0.78 ms  Limit Exceeded!
     6  206.72.210.122  0.64 ms  Limit Exceeded!
     7  184.105.81.101  9.19 ms  Limit Exceeded!
     8  72.52.104.74  9.35 ms  Limit Exceeded!
    
    
    Traceroute to United States, Las Vegas Level3 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 205.216.62.38 (205.216.62.38), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  0.66 ms  Limit Exceeded!
     6  89.149.183.38  1.16 ms  Limit Exceeded!
     7  *
     8  *
     9  *
    10  67.14.54.178  37.42 ms  Limit Exceeded!
    11  216.34.172.42  33.43 ms  Limit Exceeded!
    12  216.34.172.42  33.33 ms  Limit Exceeded!
    13  216.39.66.3  38.96 ms  Limit Exceeded!
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
    
    
    Traceroute to United States, San Jose ZAYO (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 64.125.191.31 (64.125.191.31), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  1.01 ms  Limit Exceeded!
     6  89.149.128.174  0.92 ms  Limit Exceeded!
     7  *
     8  *
     9  64.125.26.182  41.77 ms  Limit Exceeded!
    10  64.125.28.102  41.57 ms  Limit Exceeded!
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
    
    
    Traceroute to United States, Ashburn Cogentco (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 149.127.109.166 (149.127.109.166), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  2.90 ms  Limit Exceeded!
     6  129.250.2.161  2.14 ms  Limit Exceeded!
     7  *
     8  154.54.25.149  1.04 ms  Limit Exceeded!
     9  154.54.45.161  11.15 ms  Limit Exceeded!
    10  154.54.45.161  10.75 ms  Limit Exceeded!
    11  154.54.42.66  19.27 ms  Limit Exceeded!
    12  154.54.28.129  49.84 ms  Limit Exceeded!
    13  154.54.24.221  59.38 ms  Limit Exceeded!
    14  154.54.7.157  59.45 ms  Limit Exceeded!
    15  154.54.46.194  60.61 ms  Limit Exceeded!
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
    
    
    Traceroute to German, Telekom (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 80.146.191.1 (80.146.191.1), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  2.19 ms  Limit Exceeded!
     6  89.149.140.253  138.49 ms  Limit Exceeded!
     7  *
     8  129.250.3.147  11.97 ms  Limit Exceeded!
     9  62.115.112.245  143.60 ms  Limit Exceeded!
    10  80.157.203.93  9.97 ms  Limit Exceeded!
    11  91.23.215.105  163.24 ms  Limit Exceeded!
    12  80.146.191.1  166.91 ms  Limit Exceeded!
    
    
    Traceroute to German, Frankfurt O2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 82.113.108.25 (82.113.108.25), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.47 ms  Limit Exceeded!
     6  213.200.120.106  29.52 ms  Limit Exceeded!
     7  129.250.7.68  28.50 ms  Limit Exceeded!
     8  *
     9  *
    10  *
    11  213.140.35.239  141.75 ms  Limit Exceeded!
    12  176.52.248.120  156.23 ms  Limit Exceeded!
    13  176.52.252.33  147.45 ms  Limit Exceeded!
    14  176.52.252.29  145.05 ms  Limit Exceeded!
    15  62.53.0.198  153.36 ms  Limit Exceeded!
    16  62.53.236.49  146.11 ms  Limit Exceeded!
    17  62.53.236.53  146.92 ms  Limit Exceeded!
    18  82.113.108.25  149.52 ms  Limit Exceeded!
    
    
    Traceroute to German, Frankfurt Vodafone (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 139.7.146.11 (139.7.146.11), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  0.51 ms  Limit Exceeded!
     6  129.250.2.117  0.51 ms  Limit Exceeded!
     7  195.2.2.154  145.11 ms  Limit Exceeded!
     8  129.250.193.222  0.44 ms  Limit Exceeded!
     9  195.2.9.41  144.90 ms  Limit Exceeded!
    10  195.2.24.246  130.45 ms  Limit Exceeded!
    11  195.2.9.41  144.66 ms  Limit Exceeded!
    12  195.2.18.190  145.97 ms  Limit Exceeded!
    13  145.253.5.57  186.89 ms  Limit Exceeded!
    14  145.253.5.57  144.49 ms  Limit Exceeded!
    15  *
    16  *
    17  *
    18  *
    19  *
    20  139.7.146.11  146.05 ms  Limit Exceeded!
    
    
    Traceroute to German, Frankfurt China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 118.85.205.101 (118.85.205.101), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  218.30.54.72  4.27 ms  Limit Exceeded!
     7  202.97.50.25  1.41 ms  Limit Exceeded!
     8  202.97.49.130  70.20 ms  Limit Exceeded!
     9  202.97.49.130  67.86 ms  Limit Exceeded!
    10  118.85.205.101  146.25 ms  Limit Exceeded!
    
    
    Traceroute to German, Frankfurt China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 5.10.138.33 (5.10.138.33), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.44 ms  Limit Exceeded!
     6  *
     7  62.115.119.129  1.03 ms  Limit Exceeded!
     8  62.115.121.221  57.84 ms  Limit Exceeded!
     9  62.115.136.200  63.93 ms  Limit Exceeded!
    10  62.115.120.239  130.68 ms  Limit Exceeded!
    11  62.115.122.189  134.87 ms  Limit Exceeded!
    12  80.239.193.226  145.01 ms  Limit Exceeded!
    13  *
    14  5.10.138.33  157.10 ms  Limit Exceeded!
    
    
    Traceroute to German, Frankfurt GTT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 213.200.65.70 (213.200.65.70), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.38 ms  Limit Exceeded!
     6  76.74.41.89  1.49 ms  Limit Exceeded!
     7  213.200.65.70  149.35 ms  Limit Exceeded!
    
    
    Traceroute to German, FrankfurtCogentco (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 212.20.150.5 (212.20.150.5), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.50 ms  Limit Exceeded!
     6  62.115.119.129  1.00 ms  Limit Exceeded!
     7  *
     8  154.54.9.29  1.16 ms  Limit Exceeded!
     9  154.54.25.149  0.67 ms  Limit Exceeded!
    10  154.54.42.78  19.44 ms  Limit Exceeded!
    11  154.54.42.78  19.22 ms  Limit Exceeded!
    12  154.54.28.129  50.01 ms  Limit Exceeded!
    13  154.54.24.221  114.53 ms  Limit Exceeded!
    14  154.54.7.157  59.55 ms  Limit Exceeded!
    15  154.54.85.246  152.95 ms  Limit Exceeded!
    16  66.28.4.198  142.90 ms  Limit Exceeded!
    17  154.54.58.233  150.36 ms  Limit Exceeded!
    18  212.20.150.5  151.17 ms  Limit Exceeded!
    
    
    Traceroute to United Kingdom, Vodafone (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 194.62.232.211 (194.62.232.211), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  76.74.41.89  0.84 ms  Limit Exceeded!
     6  62.115.119.40  0.65 ms  Limit Exceeded!
     7  129.250.2.186  1.38 ms  Limit Exceeded!
     8  129.250.193.222  0.42 ms  Limit Exceeded!
     9  195.2.24.33  132.95 ms  Limit Exceeded!
    10  *
    11  *
    12  *
    13  *
    14  194.62.232.211  133.99 ms  Limit Exceeded!
    
    
    Traceroute to United Kingdom， BT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 213.121.43.24 (213.121.43.24), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.193  0.32 ms  Limit Exceeded!
     6  62.115.119.129  0.90 ms  Limit Exceeded!
     7  129.250.3.188  61.20 ms  Limit Exceeded!
     8  62.115.136.200  62.36 ms  Limit Exceeded!
     9  129.250.3.215  130.21 ms  Limit Exceeded!
    10  62.6.201.249  152.61 ms  Limit Exceeded!
    11  166.49.214.195  136.80 ms  Limit Exceeded!
    12  109.159.252.231  137.53 ms  Limit Exceeded!
    13  *
    14  62.6.201.174  141.76 ms  Limit Exceeded!
    15  194.72.7.101  138.59 ms  Limit Exceeded!
    16  *
    17  *
    18  213.121.43.24  156.66 ms  Limit Exceeded!
    
    
    Traceroute to United Kingdom, London TATA (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 80.231.131.34 (80.231.131.34), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  129.250.207.189  2.62 ms  Limit Exceeded!
     6  129.250.2.161  0.45 ms  Limit Exceeded!
     7  129.250.4.107  0.88 ms  Limit Exceeded!
     8  129.250.9.18  0.98 ms  Limit Exceeded!
     9  216.6.87.110  61.62 ms  Limit Exceeded!
    10  216.6.87.43  68.09 ms  Limit Exceeded!
    11  216.6.87.43  63.61 ms  Limit Exceeded!
    12  80.231.130.25  131.34 ms  Limit Exceeded!
    13  80.231.130.25  131.85 ms  Limit Exceeded!
    14  80.231.131.34  132.91 ms  Limit Exceeded!
    
    
    Traceroute to Russia, China CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 118.85.205.181 (118.85.205.181), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  218.30.54.72  3.56 ms  Limit Exceeded!
     7  202.97.83.241  2.73 ms  Limit Exceeded!
     8  202.97.59.141  154.88 ms  Limit Exceeded!
     9  202.97.59.141  152.38 ms  Limit Exceeded!
    10  *
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
    
    
    Traceroute to Russia, China CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 185.75.173.17 (185.75.173.17), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.43 ms  Limit Exceeded!
     6  62.115.149.36  0.42 ms  Limit Exceeded!
     7  62.115.121.221  57.48 ms  Limit Exceeded!
     8  62.115.136.200  62.55 ms  Limit Exceeded!
     9  62.115.136.200  60.16 ms  Limit Exceeded!
    10  62.115.120.239  132.90 ms  Limit Exceeded!
    11  62.115.122.189  134.70 ms  Limit Exceeded!
    12  *
    13  185.75.173.17  194.18 ms  Limit Exceeded!
    
    
    Traceroute to Russia, Moscow RT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 87.226.162.77 (87.226.162.77), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  76.74.41.89  12.13 ms  Limit Exceeded!
     7  77.67.90.99  146.23 ms  Limit Exceeded!
     8  77.67.90.99  146.09 ms  Limit Exceeded!
     9  87.226.140.2  188.08 ms  Limit Exceeded!
    10  *
    11  *
    12  87.226.162.77  175.70 ms  Limit Exceeded!
    
    
    Traceroute to Russia, Moscow TTK (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 217.150.32.2 (217.150.32.2), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  62.115.149.36  0.50 ms  Limit Exceeded!
     6  62.115.149.36  0.50 ms  Limit Exceeded!
     7  62.115.137.36  144.50 ms  Limit Exceeded!
     8  62.115.122.158  144.52 ms  Limit Exceeded!
     9  *
    10  62.115.123.12  151.08 ms  Limit Exceeded!
    11  62.115.124.25  148.31 ms  Limit Exceeded!
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
    
    
    Traceroute to Russia, Moscow MTS (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 195.34.32.71 (195.34.32.71), 30 hops max, 32 byte packets
     1  *
     2  *
     3  *
     4  *
     5  *
     6  212.188.28.129  153.87 ms  Limit Exceeded!
     7  195.34.59.113  152.37 ms  Limit Exceeded!
     8  212.188.42.102  160.01 ms  Limit Exceeded!
     9  195.34.50.145  191.07 ms  Limit Exceeded!
    10  195.34.50.74  188.68 ms  Limit Exceeded!
    11  195.34.50.74  187.46 ms  Limit Exceeded!
    12  195.34.53.253  186.95 ms  Limit Exceeded!
    13  195.34.53.253  188.19 ms  Limit Exceeded!
    14  195.34.32.71  193.64 ms  Limit Exceeded!
    
    
     -> Traceroute Test (IPV6)
    
    Traceroute to China, Beijing CU IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2408:80f0:4100:2005::3 (2408:80f0:4100:2005::3), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.76 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  1.20 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1fa  10.87 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  0.93 ms  Limit Exceeded!
     6  2001:2000:3080:100a::1  3.73 ms  Limit Exceeded!
     7  2001:2034:1:74::1  151.01 ms  Limit Exceeded!
     8  2001:2034:1:be::1  146.88 ms  Limit Exceeded!
     9  2001:2034:1:c1::1  146.33 ms  Limit Exceeded!
    10  2001:2034:1:6c::1  147.98 ms  Limit Exceeded!
    11  *
    12  2408:8000:2:8030::  222.54 ms  Limit Exceeded!
    13  *
    14  *
    15  2408:8000:2:685::  322.95 ms  Limit Exceeded!
    16  2408:8000:1100:306::3  323.54 ms  Limit Exceeded!
    17  2408:8000:1100:306::3  329.75 ms  Limit Exceeded!
    18  2408:8000:1f10:3d00::3  373.42 ms  Limit Exceeded!
    19  2408:80f0:4100:2006::1  326.19 ms  Limit Exceeded!
    20  2408:80f0:4100:2006::b  329.54 ms  Limit Exceeded!
    21  2408:80f0:4100:2006::b  331.60 ms  Limit Exceeded!
    22  2408:80f0:4100:2005::3  325.56 ms  Limit Exceeded!
    
    Traceroute to China, Beijing CT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2400:da00:2::29 (2400:da00:2::29), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.72 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.08 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1f1  1.11 ms  Limit Exceeded!
     5  2001:504:13::1a  0.60 ms  Limit Exceeded!
     6  2001:504:13::1a  0.54 ms  Limit Exceeded!
     7  2001:7fa:0:1::ca28:a1be  195.22 ms  Limit Exceeded!
     8  2001:252:0:108::1  303.08 ms  Limit Exceeded!
     9  *
    10  *
    11  2001:da8:2:801::2  468.64 ms  Limit Exceeded!
    12  2001:da8:2:801::2  451.80 ms  Limit Exceeded!
    13  2400:a980:ff:76::2  450.01 ms  Limit Exceeded!
    14  *
    15  240c:4001::182:61:255:2  520.08 ms  Limit Exceeded!
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
    
    Traceroute to China, Beijing CM IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2409:8089:1020:50ff:1000::fd01 (2409:8089:1020:50ff:1000::fd01), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.68 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  1.33 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  7.67 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f6  1.04 ms  Limit Exceeded!
     6  2001:668:0:3:ffff:2:0:18f1  13.72 ms  Limit Exceeded!
     7  2001:668:0:2:ffff:0:5995:b566  12.36 ms  Limit Exceeded!
     8  *
     9  2402:4f00:1000:100::51d  151.08 ms  Limit Exceeded!
    10  2402:4f00:1000:100::12e  266.28 ms  Limit Exceeded!
    11  2409:8080:0:4:2f1:292::  267.60 ms  Limit Exceeded!
    12  2409:8080:0:1:2c1:2f1:1:0  323.48 ms  Limit Exceeded!
    13  2409:8080:0:1:203:2c1::  323.16 ms  Limit Exceeded!
    14  2409:8080:0:1:103:407:0:1  349.15 ms  Limit Exceeded!
    15  2409:8080:0:2:103:1b1:0:1  349.65 ms  Limit Exceeded!
    16  2409:8089:1020:50ff:1000::fd01  352.04 ms  Limit Exceeded!
    
    Traceroute to China, Shanghai CU IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2408:8000:9000:20e6::b7 (2408:8000:9000:20e6::b7), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.69 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.14 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  2.07 ms  Limit Exceeded!
     5  2001:2000:3080:100a::1  0.42 ms  Limit Exceeded!
     6  2001:2034:0:16e::1  150.93 ms  Limit Exceeded!
     7  2001:2034:1:74::1  151.06 ms  Limit Exceeded!
     8  2001:2034:1:be::1  146.08 ms  Limit Exceeded!
     9  2001:2034:1:6c::1  145.90 ms  Limit Exceeded!
    10  2001:2034:1:6c::1  145.68 ms  Limit Exceeded!
    11  *
    12  2408:8000:2:8033::  242.80 ms  Limit Exceeded!
    13  *
    14  *
    15  *
    16  2408:8000:2:686::  343.55 ms  Limit Exceeded!
    17  2408:8000:9000:20e6::b7  345.97 ms  Limit Exceeded!
    
    Traceroute to China, Shanghai CT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 240e:18:10:a01::1 (240e:18:10:a01::1), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.75 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  2.44 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1fa  33.57 ms  Limit Exceeded!
     5  2001:668:0:3:ffff:2:0:18f1  0.64 ms  Limit Exceeded!
     6  2001:668:0:2:ffff:0:d5c8:7cb2  0.99 ms  Limit Exceeded!
     7  2001:550:3::1c5  1.08 ms  Limit Exceeded!
     8  2001:550:2:18::15b:2  7.36 ms  Limit Exceeded!
     9  *
    10  240e:0:a::cb:3ab0  226.94 ms  Limit Exceeded!
    11  240e:0:a::c9:ccc  247.01 ms  Limit Exceeded!
    12  *
    13  240e:18:1:4045::89  249.98 ms  Limit Exceeded!
    14  240e:18:10:1458::89  247.19 ms  Limit Exceeded!
    15  240e:18:10:a01::1  250.86 ms  Limit Exceeded!
    
    Traceroute to China, Shanghai CM IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2409:801e:5c03:2000::207 (2409:801e:5c03:2000::207), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.72 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  1.48 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1f1  12.17 ms  Limit Exceeded!
     5  2001:504:13::1a  0.64 ms  Limit Exceeded!
     6  2001:504:13::1a  0.50 ms  Limit Exceeded!
     7  2402:4f00:1000:100::b1  157.99 ms  Limit Exceeded!
     8  2402:4f00:1000:100::b1  158.01 ms  Limit Exceeded!
     9  2409:8080:0:4:2f1:291::  269.98 ms  Limit Exceeded!
    10  *
    11  2409:8080:0:1:2c1:2f1:3:0  321.99 ms  Limit Exceeded!
    12  2409:8080:0:1:201:2c1::  321.14 ms  Limit Exceeded!
    13  2409:8080:0:2:201:275:0:1  321.69 ms  Limit Exceeded!
    14  2409:801e:5c01:2000::31  324.57 ms  Limit Exceeded!
    15  *
    16  2409:801e:5c03:2000::207  322.22 ms  Limit Exceeded!
    
    Traceroute to China, Guangzhou CU IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2408:8001:3011:310::3 (2408:8001:3011:310::3), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.66 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.22 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.29 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  14.31 ms  Limit Exceeded!
     6  2001:2034:0:16e::1  150.92 ms  Limit Exceeded!
     7  2001:2034:0:16e::1  151.14 ms  Limit Exceeded!
     8  2001:2034:1:c1::1  144.82 ms  Limit Exceeded!
     9  2001:2034:1:6c::1  147.53 ms  Limit Exceeded!
    10  2001:2034:1:6b::1  148.56 ms  Limit Exceeded!
    11  *
    12  2408:8000:3::24c  225.79 ms  Limit Exceeded!
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
    
    Traceroute to China, Guangzhou CT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 240e:ff:e02c:1:21:: (240e:ff:e02c:1:21::), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.74 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:331  0.90 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  1.00 ms  Limit Exceeded!
     5  2001:668:0:3:ffff:2:0:18f1  0.67 ms  Limit Exceeded!
     6  2001:668:0:2:ffff:0:d5c8:7cb2  1.45 ms  Limit Exceeded!
     7  *
     8  2001:550:2:18::15b:2  7.33 ms  Limit Exceeded!
     9  240e:0:a::db:3218  7.22 ms  Limit Exceeded!
    10  240e:0:a::cb:2be8  247.80 ms  Limit Exceeded!
    11  240e:0:a::c9:2198  235.61 ms  Limit Exceeded!
    12  *
    13  *
    14  240e:1f:5000:6::3  333.53 ms  Limit Exceeded!
    15  240e:1f:5807:1::3  343.49 ms  Limit Exceeded!
    16  240e:ff:e02c::1  327.81 ms  Limit Exceeded!
    17  *
    18  240e:ff:e02c:1:21::  311.15 ms  Limit Exceeded!
    
    Traceroute to China, Guangzhou CM IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2409:8057:5c00:30::6 (2409:8057:5c00:30::6), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.59 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.17 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.37 ms  Limit Exceeded!
     5  2001:504:13::1a  3.51 ms  Limit Exceeded!
     6  2001:504:13::219  158.28 ms  Limit Exceeded!
     7  2001:504:13::219  158.14 ms  Limit Exceeded!
     8  2402:4f00:1000:100::3da  185.64 ms  Limit Exceeded!
     9  2409:8080:0:4:2f1:291::  270.07 ms  Limit Exceeded!
    10  2409:8080:0:1:2c1:2f1:4:0  319.94 ms  Limit Exceeded!
    11  2409:8080:0:1:2c1:2f1:4:0  319.47 ms  Limit Exceeded!
    12  *
    13  2409:8080:1:2:301:1103::  347.43 ms  Limit Exceeded!
    14  *
    15  2409:8080:1:2:301:375:1:1  352.18 ms  Limit Exceeded!
    16  *
    17  2409:8055:1:b300::  369.29 ms  Limit Exceeded!
    18  2409:8055:5c00:0:4c00::1  368.92 ms  Limit Exceeded!
    19  *
    20  *
    21  *
    22  *
    23  2409:8057:5c00:30::6  366.35 ms  Limit Exceeded!
    
    Traceroute to China, Beijing Dr.Peng IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2403:8880:400f::2 (2403:8880:400f::2), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.61 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:331  1.17 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  1.25 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  66.06 ms  Limit Exceeded!
     6  2001:504:13::1a  61.56 ms  Limit Exceeded!
     7  2001:470:0:3bf::2  154.06 ms  Limit Exceeded!
     8  2001:7fa:0:1::ca28:a1be  195.20 ms  Limit Exceeded!
     9  2001:252:0:106::1  225.08 ms  Limit Exceeded!
    10  *
    11  2001:252:0:1::1  355.10 ms  Limit Exceeded!
    12  2001:da8:2:801::2  346.80 ms  Limit Exceeded!
    13  2400:a980:ff:29::2  342.45 ms  Limit Exceeded!
    14  2403:8880:400f::2  327.78 ms  Limit Exceeded!
    
    Traceroute to China, Beijing CERNET2 IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:da8:a0:1001::1 (2001:da8:a0:1001::1), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.62 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.53 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  0.96 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  1.02 ms  Limit Exceeded!
     6  2001:504:13::1a  0.69 ms  Limit Exceeded!
     7  2001:470:0:3bf::2  154.04 ms  Limit Exceeded!
     8  2001:7fa:0:1::ca28:a1be  194.44 ms  Limit Exceeded!
     9  2001:252:0:106::1  211.79 ms  Limit Exceeded!
    10  *
    11  2001:252:0:1::1  323.43 ms  Limit Exceeded!
    12  2001:da8:a0:1001::1  308.63 ms  Limit Exceeded!
    
    Traceroute to China, Beijing CSTNET IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2400:dd00:0:37::213 (2400:dd00:0:37::213), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.60 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.11 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.00 ms  Limit Exceeded!
     5  2001:504:13::1a  0.76 ms  Limit Exceeded!
     6  2001:470:0:3bf::2  156.79 ms  Limit Exceeded!
     7  2001:7fa:0:1::ca28:a1be  190.77 ms  Limit Exceeded!
     8  2001:252:0:106::1  206.32 ms  Limit Exceeded!
     9  *
    10  *
    11  2400:dd00:0:4::200  331.03 ms  Limit Exceeded!
    12  2400:dd00:0:37::213  334.40 ms  Limit Exceeded!
    
    Traceroute to China, Hongkong HKIX IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:7fa:0:1::ca28:a1a9 (2001:7fa:0:1::ca28:a1a9), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.73 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:331  0.93 ms  Limit Exceeded!
     4  *
     5  *
     6  *
     7  *
     8  *
     9  *
    10  *
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
    
    Traceroute to China, Hongkong HE IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:470:0:490::2 (2001:470:0:490::2), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.78 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:331  1.44 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  1.08 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  1.35 ms  Limit Exceeded!
     6  2001:504:13::1a  0.67 ms  Limit Exceeded!
     7  2001:470:0:3bf::2  154.05 ms  Limit Exceeded!
     8  2001:470:0:490::2  160.22 ms  Limit Exceeded!
    
    Traceroute to United States, San Jose HE IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:470:1:ff::1 (2001:470:1:ff::1), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.74 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.17 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.24 ms  Limit Exceeded!
     5  2001:504:13::1a  0.54 ms  Limit Exceeded!
     6  2001:470:0:347::1  9.00 ms  Limit Exceeded!
     7  2001:470:1:ff::1  41.37 ms  Limit Exceeded!
    
    Traceroute to United States, Chicago NTT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:418:0:5000::1026 (2001:418:0:5000::1026), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.75 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:325  1.52 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1fa  1.08 ms  Limit Exceeded!
     5  2001:418:0:5000::1011  0.53 ms  Limit Exceeded!
     6  *
     7  2001:418:0:2000::111  8.32 ms  Limit Exceeded!
     8  2001:418:0:2000::79  68.32 ms  Limit Exceeded!
     9  2001:418:0:2000::1e2  57.38 ms  Limit Exceeded!
    10  2001:418:0:5000::1026  57.29 ms  Limit Exceeded!
    
    Traceroute to United States, Los Angeles Telia IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:2000:3080:1e96::2 (2001:2000:3080:1e96::2), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.65 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  1.42 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  11.42 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  1.13 ms  Limit Exceeded!
     6  2001:2000:3080:100a::1  0.42 ms  Limit Exceeded!
     7  *
     8  2001:2000:3080:1e96::2  1.29 ms  Limit Exceeded!
    
    Traceroute to United States, Los Angeles GTT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:668:0:3:ffff:0:d8dd:9d5a (2001:668:0:3:ffff:0:d8dd:9d5a), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.61 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.45 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  19.08 ms  Limit Exceeded!
     5  *
     6  *
     7  *
     8  *
     9  *
    10  *
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
    
    Traceroute to United States, Kansas City Sprint IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2600:0:1:1239:144:228:241:71 (2600:0:1:1239:144:228:241:71), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.72 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.27 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.58 ms  Limit Exceeded!
     5  2001:2000:3080:100a::1  0.57 ms  Limit Exceeded!
     6  2600:0:3:1239:144:232:0:a9  0.56 ms  Limit Exceeded!
     7  2600:0:2:1239:144:232:22:162  3.47 ms  Limit Exceeded!
     8  2600:0:2:1239:144:232:13:82  29.90 ms  Limit Exceeded!
     9  2600:0:2:1239:144:232:8:167  11.46 ms  Limit Exceeded!
    10  2600:0:1:1239:144:228:241:71  42.36 ms  Limit Exceeded!
    
    Traceroute to United States, Los Angeles Verizon IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2600:80a:2::15 (2600:80a:2::15), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.65 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  18.14 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1fa  1.08 ms  Limit Exceeded!
     5  2001:418:0:5000::1011  0.62 ms  Limit Exceeded!
     6  *
     7  2001:418:0:2000::285  4.72 ms  Limit Exceeded!
     8  2600:80a:2::15  1.28 ms  Limit Exceeded!
    
    Traceroute to United Status, Ashburn Cogentco IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:550:0:1000::9a36:4215 (2001:550:0:1000::9a36:4215), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.70 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.49 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  7.13 ms  Limit Exceeded!
     5  2001:418:0:5000::1015  0.39 ms  Limit Exceeded!
     6  2001:418:0:2000::28a  1.47 ms  Limit Exceeded!
     7  2001:418:0:2000::11a  1.29 ms  Limit Exceeded!
     8  *
     9  *
    10  *
    11  *
    12  2001:550:0:1000::9a36:1ddd  37.95 ms  Limit Exceeded!
    13  *
    14  2001:550:0:1000::9a36:4215  60.21 ms  Limit Exceeded!
    
    Traceroute to United States, San Jose Level3 IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:1900:2100::2eb5 (2001:1900:2100::2eb5), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.63 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:335  1.46 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:1fa  0.98 ms  Limit Exceeded!
     5  2001:19f0:6000::a44:1f5  1.64 ms  Limit Exceeded!
     6  2001:1900:2100::40d9  0.61 ms  Limit Exceeded!
     7  2001:1900:2100::2eb5  10.86 ms  Limit Exceeded!
    
    Traceroute to United States, Seattle Zayo IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:438:ffff::407d:d6a (2001:438:ffff::407d:d6a), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.70 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:331  1.05 ms  Limit Exceeded!
     4  2001:19f0:6000::a44:cd  1.10 ms  Limit Exceeded!
     5  2001:668:0:3:ffff:2:0:18f1  5.81 ms  Limit Exceeded!
     6  2001:668:0:2:ffff:0:5995:bb66  0.87 ms  Limit Exceeded!
     7  2001:668:0:3:ffff:0:d178:8c56  0.58 ms  Limit Exceeded!
     8  2001:438:ffff::407d:1d69  27.18 ms  Limit Exceeded!
     9  2001:438:ffff::407d:d6a  30.38 ms  Limit Exceeded!
    
    Traceroute to France, Paris HE IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:470:0:349::1 (2001:470:0:349::1), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:b::6464:c801  0.74 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  1.53 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.40 ms  Limit Exceeded!
     5  2001:504:13::1a  0.68 ms  Limit Exceeded!
     6  2001:504:13::1a  0.61 ms  Limit Exceeded!
     7  2001:470:0:324::1  55.03 ms  Limit Exceeded!
     8  2001:470:0:299::2  63.16 ms  Limit Exceeded!
     9  2001:470:0:349::1  132.60 ms  Limit Exceeded!
    
    Traceroute to German, Frankfurt NTT IPV6 (ICMP Mode, Max 30 Hop)
    ============================================================
    traceroute to 2001:728:0:5000::6f6 (2001:728:0:5000::6f6), 30 hops max, 32 byte packets
     1  *
     2  2001:19f0:fc01:a::6464:6401  0.65 ms  Limit Exceeded!
     3  2001:19f0:fc00::a44:319  22.04 ms  Limit Exceeded!
     4  2001:19f0:fc00::a44:506  1.32 ms  Limit Exceeded!
     5  2001:418:0:5000::1011  0.67 ms  Limit Exceeded!
     6  2001:418:0:2000::29e  4.71 ms  Limit Exceeded!
     7  2001:418:0:2000::1bd  67.60 ms  Limit Exceeded!
     8  2001:418:0:2000::5d  140.50 ms  Limit Exceeded!
     9  2001:728:0:2000::15e  156.63 ms  Limit Exceeded!
    10  2001:728:0:2000::25e  153.36 ms  Limit Exceeded!
    11  2001:728:0:5000::6f6  150.23 ms  Limit Exceeded!



  [1]: https://www.vultr.com/?ref=8833279
  [2]: https://www.vultr.com
  [3]: http://lax-ca-us-ping.vultr.com/
  [4]: https://www.vultr.com/legal/tos/
