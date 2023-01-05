---
title: mac使用
top: false
cover: false
toc: true
mathjax: false
date: 2022-03-06 00:24:35
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

- 更新 brew 源 
  https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/
  https://blog.csdn.net/claram/article/details/101577547
- 使用sshfs
  https://www.jianshu.com/p/59b642c8820b?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation
- 远程挂载磁盘
  https://setapp.com/how-to/map-a-network-drive-on-mac



# 关键指令使用

- sshfs挂在远程磁盘

  sshfs -C -o reconnect tianshan@192.168.18.7 mount_remote

# 遇到的问题

- 安装服务器挂载工具 sshfs 报错 Error: sshfs has been disabled because it requires FUSE!
  https://github.com/telepresenceio/telepresence/issues/1654
- 此tap的存在是为了支持从自制内核中删除的macOS FUSE相关软件
  https://github.com/osxfuse/osxfuse/issues/781
  https://github.com/gromgit/homebrew-fuse
- 更新系统之后无法 hexo 无法使用 解决方法： 重新安装npm





# 关闭一些弹窗

- 关闭mac的Microsoft AutoUpdate弹窗提示
  https://zhuanlan.zhihu.com/p/132658872
- 关闭Adobe Genuine Software Integrity Service
  https://keesenz.com/2020/873.html

# 卸载某些软件

- 卸载 epochCam
  https://help.elgato.com/hc/en-us/articles/360048910371-EpocCam-Uninstall



# 关于外接视频音频

- epocCam 
  ipad可以配合mac上的 epocViewer 实时显示画面，但是ipod显示不出来，但是在其他软件中可以使用，epocCam的音频无法正常使用，如果有声音回声比较严重
- mac 和 iPod 使用 usb连接，使用 麦克风 app 传输声音 ，效果较好
- 2022-03-21 结论 epocCam 和 麦克风 两个软件配合使用

# 快捷操作

- 快捷键插入日期
  
