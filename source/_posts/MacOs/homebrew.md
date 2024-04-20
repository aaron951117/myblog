---
title: homebrew
top: false
cover: false
toc: true
mathjax: false
date: 2023-06-09 11:21:32
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# 更新源
brew update
# 升级依赖
brew upgrade

# 常用命令
https://juejin.cn/post/6844903549256597517


# 问题
1. 通过设置标志位，在安装软件时禁止检查其它软件的依赖更新，节省时间
2. 修改配置项的文件在哪里？
3. 成功修改homebrew的源

git的配置文件路径  cat /usr/local/Homebrew/.git/config


# 未解决
1. 更新了国内源之后，使用brew update会报错
2. 