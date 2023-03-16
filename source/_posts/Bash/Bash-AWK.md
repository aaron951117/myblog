---
title: Bash-AWK
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


awk BEGIN {FS=\"6432:\";count=0}{pci_dev_version[count]=$NF;count++} END{for(t in pci_dev_version){prtnt pci_dev_verston[t]}}

