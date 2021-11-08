---
title: Vultr 洛杉矶 VPS 评测
date: 2021-06-01 04:21:37
tags:
- Vultr
- VPS
- 评测
categories: 商家评测
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108202311.png
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

  [1]: https://www.vultr.com/?ref=8833279
  [2]: https://www.vultr.com
  [3]: http://lax-ca-us-ping.vultr.com/
  [4]: https://www.vultr.com/legal/tos/
