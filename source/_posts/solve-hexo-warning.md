---
title: 今天优化了下 Hexo
date: 2022-02-20 20:50:09
updated: 2022-02-20 20:50:09
tags:
- hexo
category: 简单记录
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220220223334.png
---

今天好好倒腾了下 Hexo，不得不说，学了很长时间 js 了，现在就是看着 hexo 很舒服，解决问题比之前顺利太多了。

## 美化篇

美化倒是没啥好提的，都是抄大佬的美化，这次主要参考了两个大佬。

> DreamyTZK 大佬的[Hexo 博客之 butterfly 主题优雅魔改系列](https://www.antmoe.com/posts/a811d614/)
> 小冰 大佬的[教程：butterfly 主题文章双栏布局插件](https://zfe.space/post/hexo-butterfly-article-double-row.html)

其中 DreamyTZK 大佬编译好的 css 被我复制到了 GitHub 供自己引用，还拆了小冰大佬的双栏布局插件，偷了所有 css，改成了我现在这种三栏的。不得不说，还是抄着爽，不用思考，一把梭就能整的很好看。

由于原创内容过少，我就不提供 css 了，提供一组美化前和美化后的截图

{% gallery %} 
![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220220210209.png)
![](https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220220210115.png)
{% endgallery %}

嗯，我个人觉得是右边好看的，当然左边的默认样式也不差就是了

## 解决问题篇

嗯，这才是正文，不过大部分都是 Google 找到的解决方案，所以就只挂主要的解决步骤和原文链接吧，这篇文章的意义也就在此了，用作记录而非炫耀。

### highlight.js 破坏性更新导致的问题

报错如下
```log
Deprecated as of 10.7.0. highlight(lang, code, ...args) has been deprecated
```

字面意思，highlight.js 自 10.7.0 就不支持这个写法了，所以我们要做的就是指定一个版本，所以解决方法就是，在 package.json 中加入如下配置:

```js
"resolutions": {
    "highlight.js": "10.6.0"
},
```
然后重新安装依赖，果然不报错了。

### stylus 旧版本循环依赖的问题

> 解决方案来自[好一则博](https://www.haoyizebo.com/posts/710984d0/)

具体是不是循环依赖我不清楚，报错如下
```log
Accessing non-existent property 'xxx' of module exports inside circular dependency
```

解决方法是，在 package.json 添加如下配置

```js
"resolutions": {
    "stylus": "0.54.8"
},
```

### hexo 的破坏性更新带来的问题

> 解决方案来自 [Boris的备份库房](https://boriskp.github.io/upgrade-hexo-to-v5-1-1/)

报错如下
```log
WARN  Deprecated config detected: "external_link" with a Boolean value is deprecated. See https://hexo.io/docs/configuration for more details.
```

解决方法，找到 hexo 根目录的 _config.yml
```yml
external_link: true # Open external links in new tab`
```
替换为
```yml
external_link:
  enable: true # Open external links in new tab
  field: site # Apply to the whole site
  exclude: '
```

## 结语

做完了这一切，有种丰收的喜悦，令人感到心旷神怡，上次这样沉迷倒腾主题的时候，已经不记得了，只觉得青春过去的好快，想到这里，喜悦便变成了怀念。
