---
layout: post
title: "Ubuntu & Windows 双系统时间显示设置"
categories: tech
---
作为一个`Macbook`党，由于不愿意每天背沉重的电脑回家，所以在在家里捣鼓了个台式机上装上了`Ubuntu`偶尔应付下工作，同时还要装`Windows`用游戏打发时间，每次重启切换系统发现因为时区问题发现时间都会显示错误。
<!--more-->

先在`Ubuntu`上更新一下时间
```bash
sudo apt-get install ntpdate
sudo ntpdate time.windows.com
```
将时间更新到硬件上
```bash
sudo hwclock --localtime --systohc
```
关闭`Linux`重新进入`Windows`系统，发现时间正常了



