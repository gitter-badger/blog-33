---
title: 使用 JAMStack 构建 Erohub
date: 2021-09-16 16:54:11
tags: erohub
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20211108202153.png
---

# 前言 #

Erohub 是我第一个认真做下去的站点，所以在我这段时间学习前端，并将之前的玩具站点都静态化之后，我觉得我必须对 Erohub 做些什么，让他成为我真正拿得出手的作品。

于是就有了，我将 Erohub  JAMStack 化的努力。

<!--more-->


# 什么是 JAMStack #

> The modern way to build [website & app] that delivers better performance

## 概念 ##

JAMStack 中的 JAM 其实是三个词的缩写

#### J : JavaScript ####

这里是指实现动态网页效果的 JavaScript ，用于在客户端实现动态网页效果

#### A: APIs

JAMStack 的 web 应用通过  JavaScript 向后端 API 发送 AJAX 请求，而后端则会返回一些数据用于处理用户交互

#### M:Markup

网站内容的模板化标记在部署时预先构建。

所以 JAMStack 就是：**使用 JavaScript，APIs 和 Markup 三种技术来构建 Web 应用**。

## 优势 ##

#### 安全

Jamstack 将页面作为预先生成的文件提供允许只读托管进一步减少攻击，因此我不需要准备用于抵御攻击的服务器和系统。

#### 高性能

页面加载速度会影响用户体验和转换。Jamstack 站点的所有页面都已在靠近用户的 CDN 上因此无需引入昂贵或复杂的基础架构即可实现非常高的性能。

#### 维护成本低 ####

当托管复杂性降低时，维护任务也会降低。而且 Jamstack 站点是预先生成的，这意味着，任何简单的静态托管解决方案都应该能够为 Jamstack 站点提供服务。

## 为什么选用 JAMStack ##

Erohub 最初的定位是一个 **多用户的** 的图片分享平台，由于我本人的原因，我也希望它也是一个**稳定、便于维护** 的平台。

因为是多用户站点，所以我必须让 Erohub 变得易用，这就需要网站有一个完善的 CMS 系统。使用传统动态网站系统，如 WordPress 、 Typecho 无疑是非常诱人的选择，但是这种程序会在面对攻击时难以招架，不够省心，因此我选择了一个折衷方案，这就是  JAMStack 。

# 我为 Erohub JAMStack 化做的努力

## 历史包袱

Erohub 在建站一年后，文章数量就突破了 900 大关，因此我之前习惯采用的 “手动迁移” （即手动复制粘贴网站内容）会变得十分繁琐，而且用户在 Typecho 后台编辑文章的习惯已经养成，我也不好教用户用 Erohub ，因此我决定将 Typecho 作为无头 CMS（仅输出网站的数据，但是不渲染 HTML 界面的内容管理系统 ） 。但是改造 Typecho 的路途并没有太多波折，因为在 Github 上早就有了现成的让 [Typecho 支持 RESTful API 的插件](https://github.com/szj1006/typecho-api)

## 设计架构

#### 后端部分

JAMStack 应用的内容应该是部署到 CDN 上的，而用 PHP 来实现这些虽然不困难，但是无疑会增加之后更换 Typecho 主机的成本，因此我选择了一个看起来很愚蠢的方案：用 Github Action 执行我写的 Python 爬虫，来爬取 Typecho 返回的数据，并部署到 CDN 上。

#### 前端部分

我选择了 Vue.js + [Tabler](https://tabler.io/) + Axios 来构建前端界面，通过 Axios 获取部署到 CDN 上的后端数据，用 Vue 渲染 DOM ，用 Tabler 美化布局，使用 Vue-router 管理路由，有 Vue-cli 这种成熟的工具链来辅助（手把手教我）写代码，一切看起来都如行云流水般简单。

做完这一切之后，我在 Github 创建了一个私有仓库，并使用 [Vercel](https://vercel.com/)部署到全球 CDN 上。

![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic/20210916183950.png)

至此，一个 JAMStack 架构的站点，诞生了。
