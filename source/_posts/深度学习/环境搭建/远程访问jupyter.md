---
title: 远程访问jupyter
top: false
cover: false
toc: true
mathjax: false
date: 2024-03-06 19:10:03
author: TianShan
img: 
coverImg: 
password: 
summary: 
tags: 
categories:
---
# 远程访问报403
找到~/.jupyter/jupyter_lab_config.py文件，修改如下，这将允许 JupyterLab 接受来自任何 IP 地址的连接。
```python
c.ServerApp.allow_remote_access = True
c.ServerApp.ip = '0.0.0.0'
```
