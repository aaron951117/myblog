---
title: 制作deb安装包
top: false
cover: false
toc: true
mathjax: false
date: 2023-04-07 15:33:58
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

# 此情况不需要编译文件
## dpkg-deb
目标：制作将hello程序安装到/usr/bin的deb安装包
### 准备文件
#### 程序源文件
1. 创建临时文件夹 deb/hello-1.0/usr/bin （工作目录是deb/hello-1.0，/usr/bin是希望安装后程序的位置）
2. 将hello程序放入 deb/hello-1.0/usr/bin 中
#### 构建deb需要的文件
1. 新建文件夹deb/hello-1.0/DEBIAN
2. 在deb/hello-1.0/DEBIAN内新建文件control，并写入以下内容
```text
Package: hello
Version: 1.0
Section:
Priority: optional
Depends:
Suggests:
Architecture: amd64
Installed-Size: 4096
Maintainer: tianshan
Provides: tianshan
Description: hello world
```
control文件中各字段的相关含义如下
| 字段                   | 描述                                                                                          |
|----------------------|---------------------------------------------------------------------------------------------|
| 包名(Packahe)          | 包名(Packahe)字段给出软件包的名称, 这是软件包工具用以识别这个包的名称, 通常(单不是必须)和这个 Debian 软件包的名称的第一个字符串相似.              |
| 版本(Version)          | 版本(Version)字段给出上游开发者的版本号和修正版本号,                                                             |
| 平台(Architecture)     | 平台(Architecture)字段指定这个二进制包的编译硬件平台.                                                          |
| 依赖(Depends)          | 依赖(Depends)字段给出所依赖的包的列表.                                                                    |
| 安装大小(Installed-Size) | 安装大小(Installed-Size)字段说明安装这个包所需磁盘空间, 用于安装前端显示是否有足够的空间安装此程序…                                 |
| 类别(Section)          | 类别(Section)行给出此包在Debian FTP上的存储位置,上存储此包的目录名(详见Debian 的 FTP 上有哪些目录?, 第 5.1 节).               |
| 优先级(Priority)        | 优先级(Priority), 对应安装来说的重要程度, dselect 和 console-apt 一类的半智能软件可以据此对软件安装分类|
| 维护者(Maintainer)      | 维护者(Maintainer)字段给出当前维护此包负责人的电子信箱                                                           |
| 描述(Description)      | 描述(Description)字段此软件包的简要说明                                                                  |
### 打包deb
在deb文件夹下执行以下命令
```bash
dpkg-deb -b hello-1.0 hello-1.0-amd64.deb
```
### 安装deb
```bash
depg -i hello-1.0-amd64.deb
```
安装完成后可以在/usr/bin文件夹下查看是否存在hello程序