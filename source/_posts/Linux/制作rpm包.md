---
title: 模版文件
top: false
cover: false
toc: true
mathjax: false
date: 2023-04-18 14:20:54
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

`rpmbuild` 默认工作路径的确定，通常由在 `/usr/lib/rpm/macros` 这个文件里的一个叫做 `%_topdir` 的宏变量来定义。

## rpmbuild的check-rpaths问题
```bash
# 解决方案：
# vi ~/.rpmmacros
# comment this out
# case "${QA_CHECK_RPATHS:-}" in [1yY]*) /usr/lib/rpm/check-rpaths ;; esac \
```

### rpm安装
rpm不检查依赖，强制安装
rpm -ivh XXX --force --nodeps

## rpm卸载
rpm卸载时 不加rpm后缀

## 查看已安装的rpm包
- yum list installed
- rpm -qa