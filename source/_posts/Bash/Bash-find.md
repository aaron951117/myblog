---
title: Bash-find
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-15 17:36:42
author:
img:
coverImg:
password:
summary:
tags:
categories:
---
以.txt 结尾文件，并且查找深度为1
```bash
find . -name “*.txt” -maxdepth 1
```
多个条件查找
```bash
find -name *.c -or -name *.h
```
