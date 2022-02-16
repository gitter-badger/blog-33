---
title: 记一次破防瞬间
date: 2022-01-28 22:37:38
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216222509.png
---

## 起因

事情是这样的，晚上准备写点 Java web，然后 tomcat 启动失败，一看端口被占用了，但是我总觉得不对劲，之前 8080 端口被占用，我已经改过一次端口了，按理说不应该这样啊，**自从装上 kali in wsl 之后(划重点哈)**才遇到这个问题，难道是 kali？我暂且蒙古

## 尝试解决

也不是第一次碰到端口占用了，我第一反应是这么搞

```powershell
netstat -ano | findstr "8081"
tskill 应用 PID
```

然后，控制台输出了一个空行，说明 8081 端口压根没被占用，所以我？？？

行吧，我再换个端口，忍了，换成 8082 ，依旧被占用，我？？？

这时候我才明白，这根本不对劲，开发常用的端口 8080 到 8082 全都被占用了，必须马上解决，而不是简单换个端口等下次解决。

## 求助 Google

既然端口并没有被占用，那可能会是 idea 或者 tomcat 的问题，我搜索关键词 `idea 端口占用` ，所有的结果都要我 kill 掉占用端口的应用，但现在问题是，压根没有应用占用端口啊，笑死，根本找不到 PID。

然后我多加了一个关键词，`实际并没有`，总算找到了这篇文章：

[IDEA 端口占用，启动失败，提示Web server failed to start. Port 8080 was already in use.](https://www.cnblogs.com/mayhot/p/15156426.html)

> 3.更改保留端口范围
> 
> 显然我遇到的不是这个情况，经过翻阅，知道还有一种可能就是端口属于系统保留端口，也会出现这种情况

嗯？系统保留端口？然后我执行文章给的命令

```powershell
netsh interface ipv4 show excludedportrange protocol=tcp
```

果然，我看到了 7000- 9000 的很多端口都被列入了保留端口，屮。

但是我又感觉不对，我之前用的好好的，为啥突然就被加入到保留端口了？

Google 查询许久，找到这篇文章：

[关于Windows端口没被占用提示An attempt was made to access a socket in a way forbidden by its access permissions_tian2342的专栏-CSDN博客](https://blog.csdn.net/tian2342/article/details/108934646)

> 最后发现可能是因为开启了Hyper-V，导致ipv4的动态起始端口变成了1024。

所以为什么我之前开启了 Hyper-V 呢？因为我之前安装了 Kali！是的，还真的是因为 kali

## 这就完了？NO

之后我用文章后面写的设置端口占用排除的命令，就这行：

```powershell
netsh int ipv4 set dynamicport tcp start=7000 num=3000
```

重启之后，所有依赖 7000-10000 端口的应用无法启动，clash 也挂了，我当场暴毙。

最后，我为了解决区区一个端口占用，选择了恢复系统还原点，令人感慨。
