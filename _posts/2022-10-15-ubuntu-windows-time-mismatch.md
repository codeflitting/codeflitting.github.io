---
layout: post
title: "Ubuntu & Windows 双系统时间显示设置"
categories: tech
---
作为一个 Macbook 党，由于不愿意每天背沉重的电脑回家，所以在在家里捣鼓了个台式机上装上了 Ubuntu 偶尔应付下工作，同时还要装 Windows 用游戏打发时间，每次重启切换系统发现因为时区问题发现时间都会显示错误。

先在 Ubuntu 上更新一下时间
```bash
sudo apt-get install ntpdate
sudo ntpdate time.windows.com
```
将时间更新到硬件上
```bash
sudo hwclock --localtime --systohc
```
关闭 Linux 重新进入 Windows 系统，发现时间正常了

<!--more-->

Windows 与 Mac/Linux 看待系统硬件时间的方式是不一样的：
* Windows 把计算机硬件时间当作本地时间，所以在 Windows 系统中显示的时间跟 BIOS 中显示的时间是一样的。
* Linux/Unix/Mac 把计算机硬件时间当作 UTC， 所以在 Linux/Unix/Mac 系统启动后在该时间的基础上，加上电脑设置的时区数（ 比如我们在中国，它就加上 8）

因此 Linux/Unix/Mac 系统中显示的时间总是比 Windows 系统中显示的时间快 8 个小时。所以，当你在 Linux/Unix/Mac 系统中，把系统现实的时间设置正确后，其实计算机硬件时间是在这个时间上减去8小时，所以当你切换成 Windows 系统后，会发现时间慢了 8 小时。
