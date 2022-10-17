---
layout: post
title: "Macbook 更新 Launchpad 图标大小"
categories: tech
---

打开终端，复制并执行以下 4 行命令进行每行和每列的图标数量：

```bash
# 调整每一列显示图标数量，9 表示每一列显示 9 个，数字部分可根据个人喜好进行设置。
defaults write com.apple.dock springboard-columns -int 9

# 调整多少行显示图标数量，这里我用的是 6，数字部分你也可以改成 8 或其他
defaults write com.apple.dock springboard-rows -int 6

# 重置`Launchpad`
defaults write com.apple.dock ResetLaunchPad -bool TRUE

# 重启`Dock`
killall Dock
```

<!--more-->

恢复默认设置的方法，在终端`Terminal`中执行以下 4 行命令：

```bash
defaults write com.apple.dock springboard-rows Default
defaults write com.apple.dock springboard-columns Default
defaults write com.apple.dock ResetLaunchPad -bool TRUE
killall Dock
```
