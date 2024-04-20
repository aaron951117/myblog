---
title: Bash-获取执行指令后的结果
top: false
cover: false
toc: true
mathjax: false
date: 2023-05-31 11:01:41
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

#!/bin/bash

version=$(program -v 2>/dev/null)
echo "版本：$version"
