---
title: 半月湾 DC5 评测
date: 2021-06-01 04:47:10
tags: 
- VPS
- 评测
- 半月湾
categories: 商家评测
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108202210.png
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

  [1]: https://hmbcloud.com/
  [2]: https://hmbcloud.com/index.php?m=TermsOfService
