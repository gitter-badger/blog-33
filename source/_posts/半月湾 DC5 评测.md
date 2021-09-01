---
title: 半月湾 DC5 评测
date: 2021-06-01 04:47:10
tags: 
- VPS
- 评测
- 半月湾
categories: 商家评测
---

半月灣，在 2020 年由美籍华人于美国旧金山创办，提供 IPLC 等转发以及 GIA 线路的 VPS/NAT 服务。半月湾致力保障用户的隐私以及匿名性，所有服务均无需实名认证。
<!--more-->

洛杉磯 DC5，于瓦工 DC6 DC9 相隔 1ms，三网 GIA

## 相关索引 ##
官网地址：[https://hmbcloud.com/][1]
商家ToS：[https://hmbcloud.com/index.php?m=TermsOfService][2]

## 套餐详情 ##

 - 1x CPU核心
 - 2G 内存
 - 10G SAS硬盘
 - 1TB 流量
 - 500M 带宽
 - 1x 独立IPV4
 - KVM虚拟化

## 综合测试 ##

### 系统信息 ###

 - CPU型号：Intel(R) Xeon(R) CPU E5-2680 
 - CPU数量：1 vCPU
 - 虚拟化类型：KVM
 - 磁盘使用率：2.12 GB / 10.26 GB
 - 引导设备：/dev/vda1

### 网络信息 ###

 - IPV4 - ASN信息:ANCHGLOBAL-AS-AP - Anchnet Asia Limited, HK
 - IPV4 - 归属地:United States California Los Angeles

## 流媒体解锁 ##

解锁`HBO Now`、`Princess Connect Re:Dive Japan`

### CPU性能测试 (标准模式, 1-Pass @ 5sec) ###

单线程测试: 661 分

### 内存性能测试 (标准模式, 3-Pass @ 30sec) ###

 - 单线程读：11487.96 MB/s
 - 单线程写：9501.17 MB/s

### 磁盘性能测试 (4K块/1M块, Direct写入) ###

| 测试项目   | 写入速度                  | 读取速度                  |
| -------------- | ----------------------------- | ----------------------------- |
| 100MB-4K Block | 29.7 MB/s (7254 IOPS, 3.53 s) | 33.3 MB/s (8131 IOPS, 3.15 s) |
| 1GB-1M Block   | 238 MB/s (227 IOPS, 4.40 s)   | 435 MB/s (414 IOPS, 2.41 s)   |

### Speedtest.net 网速测试 ###

| 节点名称   | 上传速度 | 下载速度 | Ping延迟 |
| -------------- | ---------- | ---------- | --------- |
| 距离最近测速点 | 11.72 MB/s | 11.40 MB/s | 6.04 ms   |
| 上海电信   | 6.37 MB/s  | 12.08 MB/s | 128.93 ms |

### 路由追踪测试 ###

    Traceroute to China, Beijing CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 123.125.99.1 (123.125.99.1), 30 hops max, 32 byte packets
     1  156.236.119.129  1.03 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  10.34 ms  *  LAN Address
     3  218.30.49.153  1.12 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.182.89  127.85 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.205  132.18 ms  *  China, ChinaTelecom
     7  59.43.80.14  128.48 ms  *  China, ChinaTelecom
     8  202.97.56.161  166.27 ms  AS4134  China, ChinaTelecom
     9  202.97.57.86  151.60 ms  AS4134  China, ChinaTelecom
    10  219.158.41.25  161.17 ms  AS4837  China, ChinaUnicom
    11  219.158.3.25  160.23 ms  AS4837  China, ChinaUnicom
    12  61.49.214.46  155.13 ms  AS4808  China, Beijing, ChinaUnicom
    13  125.33.187.58  151.09 ms  AS4808  China, Beijing, ChinaUnicom
    14  124.65.194.42  188.11 ms  AS4808  China, Beijing, ChinaUnicom
    15  61.135.113.158  154.24 ms  AS4808  China, Beijing, ChinaUnicom
    16  *
    17  *
    18  123.125.99.1  154.72 ms  AS4808  China, Beijing, ChinaUnicom
    
    
    Traceroute to China, Beijing CT (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 180.149.128.9 (180.149.128.9), 30 hops max, 32 byte packets
     1  156.236.119.129  1.13 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  29.70 ms  *  LAN Address
     3  218.30.49.153  1.09 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.246.237  127.39 ms  *  China, ChinaTelecom
     5  59.43.247.101  153.93 ms  *  China, ChinaTelecom
     6  *
     7  59.43.132.17  149.73 ms  *  China, ChinaTelecom
     8  *
     9  *
    10  36.110.246.198  153.89 ms  AS23724  China, Beijing, ChinaTelecom
    11  180.149.128.9  157.43 ms  AS23724  China, Beijing, ChinaTelecom
    
    
    Traceroute to China, Beijing CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.136.25.153 (211.136.25.153), 30 hops max, 32 byte packets
     1  156.236.119.129  1.45 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  21.07 ms  *  LAN Address
     3  218.30.49.153  1.21 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.189.33  126.89 ms  *  China, ChinaTelecom
     5  59.43.187.61  125.61 ms  *  China, ChinaTelecom
     6  *
     7  59.43.80.94  127.49 ms  *  China, ChinaTelecom
     8  202.97.56.161  165.59 ms  AS4134  China, ChinaTelecom
     9  202.97.57.38  152.43 ms  AS4134  China, ChinaTelecom
    10  *
    11  221.183.94.25  178.45 ms  AS9808  China, ChinaMobile
    12  *
    13  *
    14  *
    15  211.136.63.66  185.68 ms  AS56048  China, Beijing, ChinaMobile
    16  *
    17  *
    18  *
    19  211.136.25.153  187.91 ms  AS56048  China, Beijing, ChinaMobile
    
    
    Traceroute to China, Shanghai CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.247.8.158 (58.247.8.158), 30 hops max, 32 byte packets
     1  156.236.119.129  1.50 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.23 ms  *  LAN Address
     3  218.30.49.153  1.18 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.182.89  127.88 ms  *  China, ChinaTelecom
     5  *
     6  59.43.138.49  139.80 ms  *  China, ChinaTelecom
     7  219.158.38.241  130.15 ms  AS4837  China, ChinaUnicom
     8  219.158.9.97  128.73 ms  AS4837  China, ChinaUnicom
     9  139.226.210.94  132.72 ms  AS17621  China, Shanghai, ChinaUnicom
    10  58.247.221.178  241.61 ms  AS17621  China, Shanghai, ChinaUnicom
    11  139.226.225.22  129.37 ms  AS17621  China, Shanghai, ChinaUnicom
    12  58.247.8.153  137.50 ms  AS17621  China, Shanghai, ChinaUnicom
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
     1  156.236.119.129  1.04 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.35 ms  *  LAN Address
     3  218.30.49.153  2.02 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.246.237  127.33 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.217  129.65 ms  *  China, ChinaTelecom
     7  101.95.88.58  130.07 ms  AS4812  China, Shanghai, ChinaTelecom
     8  *
     9  124.74.232.58  130.46 ms  AS4811  China, Shanghai, ChinaTelecom
    10  101.227.255.46  130.54 ms  AS4812  China, Shanghai, ChinaTelecom
    11  180.153.28.5  132.47 ms  AS4812  China, Shanghai, ChinaTelecom
    
    
    Traceroute to China, Shanghai CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 221.183.55.22 (221.183.55.22), 30 hops max, 32 byte packets
     1  156.236.119.129  1.09 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.27 ms  *  LAN Address
     3  218.30.49.153  1.36 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.189.33  126.85 ms  *  China, ChinaTelecom
     5  59.43.187.57  128.22 ms  *  China, ChinaTelecom
     6  59.43.130.193  129.49 ms  *  China, ChinaTelecom
     7  59.43.80.141  128.55 ms  *  China, ChinaTelecom
     8  202.97.87.130  132.81 ms  AS4134  China, ChinaTelecom
     9  *
    10  221.183.86.102  160.51 ms  AS9808  China, ChinaMobile
    11  111.24.3.82  165.30 ms  AS9808  China, ChinaMobile
    12  221.176.22.10  165.39 ms  AS9808  China, ChinaMobile
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
    
    
    Traceroute to China, Guangzhou CU (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.21.4.130 (210.21.4.130), 30 hops max, 32 byte packets
     1  156.236.119.129  1.07 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  17.86 ms  *  LAN Address
     3  218.30.49.153  1.08 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.246.233  154.98 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.149  160.42 ms  *  China, ChinaTelecom
     7  219.158.40.169  163.47 ms  AS4837  China, ChinaUnicom
     8  219.158.10.249  171.22 ms  AS4837  China, ChinaUnicom
     9  120.83.0.58  157.95 ms  AS17816  China, Guangdong, Guangzhou, ChinaUnicom
    10  120.80.170.254  156.12 ms  AS17622  China, Guangdong, Guangzhou, ChinaUnicom
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
     1  156.236.119.129  0.94 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.11 ms  *  LAN Address
     3  218.30.49.153  1.43 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.182.81  127.22 ms  *  China, ChinaTelecom
     5  59.43.187.73  128.00 ms  *  China, ChinaTelecom
     6  59.43.130.193  128.76 ms  *  China, ChinaTelecom
     7  59.43.80.14  130.15 ms  *  China, ChinaTelecom
     8  202.97.82.86  155.20 ms  AS4134  China, ChinaTelecom
     9  113.108.209.1  162.40 ms  AS58466  China, Guangdong, Guangzhou, ChinaTelecom
    
    
    Traceroute to China, Guangzhou CM (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 120.196.212.25 (120.196.212.25), 30 hops max, 32 byte packets
     1  156.236.119.129  1.03 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.00 ms  *  LAN Address
     3  218.30.49.153  0.88 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.182.74  150.40 ms  *  China, ChinaTelecom
     5  *
     6  59.43.130.157  158.00 ms  *  China, ChinaTelecom
     7  59.43.80.122  153.12 ms  *  China, ChinaTelecom
     8  202.97.18.233  160.55 ms  AS4134  China, ChinaTelecom
     9  *
    10  221.183.90.217  222.45 ms  AS9808  China, ChinaMobile
    11  *
    12  183.235.226.1  194.63 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    13  211.136.203.22  204.40 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    14  211.139.180.106  199.38 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    15  211.139.180.106  191.34 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    16  *
    17  *
    18  120.196.212.25  196.32 ms  AS56040  China, Guangdong, Guangzhou, ChinaMobile
    
    
    Traceroute to China, Shanghai CU AS9929 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 210.13.66.238 (210.13.66.238), 30 hops max, 32 byte packets
     1  156.236.119.129  0.98 ms  AS137443  United States, California, Los Angeles, cloudinnovation.org
     2  10.8.18.1  1.15 ms  *  LAN Address
     3  218.30.49.153  0.85 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
     4  59.43.182.89  140.84 ms  *  China, ChinaTelecom
     5  59.43.187.77  125.15 ms  *  China, ChinaTelecom
     6  59.43.138.49  133.30 ms  Limit Exceeded! (frk@ipip.net)
     7  59.43.80.141  131.39 ms  Limit Exceeded! (frk@ipip.net)
     8  202.97.46.58  130.77 ms  Limit Exceeded! (frk@ipip.net)
     9  202.97.16.66  155.81 ms  Limit Exceeded! (frk@ipip.net)
    10  218.105.2.173  154.13 ms  Limit Exceeded! (frk@ipip.net)
    11  218.105.2.210  185.60 ms  Limit Exceeded! (frk@ipip.net)
    12  210.13.116.86  163.28 ms  Limit Exceeded! (frk@ipip.net)
    13  210.13.66.237  220.99 ms  Limit Exceeded! (frk@ipip.net)
    14  210.13.66.238  161.24 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Shanghai CT CN2 (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 58.32.0.1 (58.32.0.1), 30 hops max, 32 byte packets
     1  156.236.119.129  1.04 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  1.29 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  0.79 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.246.237  127.40 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.186.245  127.86 ms  Limit Exceeded! (frk@ipip.net)
     6  59.43.138.53  136.86 ms  Limit Exceeded! (frk@ipip.net)
     7  101.95.88.34  126.36 ms  Limit Exceeded! (frk@ipip.net)
     8  101.95.95.82  128.41 ms  Limit Exceeded! (frk@ipip.net)
     9  58.32.0.1  129.68 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Guangzhou CT CN2 Gaming Broadband (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 119.121.0.1 (119.121.0.1), 30 hops max, 32 byte packets
     1  156.236.119.129  3.33 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  9.34 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  0.93 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.74  165.28 ms  Limit Exceeded! (frk@ipip.net)
     5  *
     6  59.43.130.145  156.72 ms  Limit Exceeded! (frk@ipip.net)
     7  59.43.70.6  161.09 ms  Limit Exceeded! (frk@ipip.net)
     8  119.121.0.1  154.40 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing Dr.Peng Home Network (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 14.131.128.1 (14.131.128.1), 30 hops max, 32 byte packets
     1  156.236.119.129  1.11 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  1.24 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  1.25 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.89  127.85 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.247.57  128.62 ms  Limit Exceeded! (frk@ipip.net)
     6  59.43.138.49  133.89 ms  Limit Exceeded! (frk@ipip.net)
     7  202.97.70.237  129.16 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  202.97.88.250  148.69 ms  Limit Exceeded! (frk@ipip.net)
    10  219.158.44.125  151.09 ms  Limit Exceeded! (frk@ipip.net)
    11  219.158.13.77  154.37 ms  Limit Exceeded! (frk@ipip.net)
    12  124.65.194.78  149.12 ms  Limit Exceeded! (frk@ipip.net)
    13  202.96.13.194  153.52 ms  Limit Exceeded! (frk@ipip.net)
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
     1  156.236.119.129  1.37 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  25.38 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  0.80 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.89  127.81 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.187.77  125.02 ms  Limit Exceeded! (frk@ipip.net)
     6  *
     7  59.43.80.94  129.16 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  202.97.88.229  148.74 ms  Limit Exceeded! (frk@ipip.net)
    10  *
    11  219.158.103.209  154.93 ms  Limit Exceeded! (frk@ipip.net)
    12  *
    13  202.96.13.242  150.85 ms  Limit Exceeded! (frk@ipip.net)
    14  *
    15  218.241.244.2  148.28 ms  Limit Exceeded! (frk@ipip.net)
    16  124.205.97.138  155.90 ms  Limit Exceeded! (frk@ipip.net)
    17  218.241.254.242  158.73 ms  Limit Exceeded! (frk@ipip.net)
    18  218.241.245.54  158.67 ms  Limit Exceeded! (frk@ipip.net)
    19  *
    20  211.167.230.100  151.85 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CERNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 202.205.109.205 (202.205.109.205), 30 hops max, 32 byte packets
     1  156.236.119.129  7.69 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  35.38 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  0.93 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.74  150.23 ms  Limit Exceeded! (frk@ipip.net)
     5  *
     6  59.43.130.109  166.46 ms  Limit Exceeded! (frk@ipip.net)
     7  *
     8  202.97.95.114  162.91 ms  Limit Exceeded! (frk@ipip.net)
     9  *
    10  101.4.117.33  175.71 ms  Limit Exceeded! (frk@ipip.net)
    11  101.4.112.38  164.96 ms  Limit Exceeded! (frk@ipip.net)
    12  101.4.117.38  186.66 ms  Limit Exceeded! (frk@ipip.net)
    13  101.4.112.1  184.66 ms  Limit Exceeded! (frk@ipip.net)
    14  101.4.113.110  193.11 ms  Limit Exceeded! (frk@ipip.net)
    15  219.224.102.230  197.67 ms  Limit Exceeded! (frk@ipip.net)
    16  202.112.38.82  193.34 ms  Limit Exceeded! (frk@ipip.net)
    17  202.205.109.205  189.08 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing CSTNET (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 159.226.254.1 (159.226.254.1), 30 hops max, 32 byte packets
     1  156.236.119.129  0.97 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  1.17 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  1.05 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.89  127.75 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.248.241  162.10 ms  Limit Exceeded! (frk@ipip.net)
     6  59.43.130.193  131.44 ms  Limit Exceeded! (frk@ipip.net)
     7  59.43.80.78  133.85 ms  Limit Exceeded! (frk@ipip.net)
     8  202.97.46.22  131.45 ms  Limit Exceeded! (frk@ipip.net)
     9  *
    10  211.102.30.22  129.43 ms  Limit Exceeded! (frk@ipip.net)
    11  159.226.254.1  171.94 ms  Limit Exceeded! (frk@ipip.net)
    
    
    Traceroute to China, Beijing GCable (TCP Mode, Max 30 Hop)
    ============================================================
    traceroute to 211.156.140.17 (211.156.140.17), 30 hops max, 32 byte packets
     1  156.236.119.129  9.85 ms  Limit Exceeded! (frk@ipip.net)
     2  10.8.18.1  0.96 ms  Limit Exceeded! (frk@ipip.net)
     3  218.30.49.153  1.07 ms  Limit Exceeded! (frk@ipip.net)
     4  59.43.182.89  127.81 ms  Limit Exceeded! (frk@ipip.net)
     5  59.43.247.125  165.56 ms  Limit Exceeded! (frk@ipip.net)
     6  *
     7  59.43.132.13  148.76 ms  Limit Exceeded! (frk@ipip.net)
     8  *
     9  106.120.252.154  156.21 ms  Limit Exceeded! (frk@ipip.net)
    10  60.247.93.254  148.37 ms  Limit Exceeded! (frk@ipip.net)
    11  211.156.128.249  152.76 ms  Limit Exceeded! (frk@ipip.net)
    12  211.156.128.85  156.17 ms  Limit Exceeded! (frk@ipip.net)
    13  211.156.140.17  152.30 ms  Limit Exceeded! (frk@ipip.net)

  [1]: https://hmbcloud.com/
  [2]: https://hmbcloud.com/index.php?m=TermsOfService
