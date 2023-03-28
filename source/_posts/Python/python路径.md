---
title: 
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-23 17:03:14
author:TianShan
img: 
coverImg: 
password: 
summary: 
tags: 
categories: 
---

# 打印当前python解释器的路径
```python
import sys
pythonpath = sys.executable
print(pythonpath)
```

# matplotlib路径
```python
import matplotlib  
print(matplotlib.matplotlib_fname())  
print(matplotlib.get_cachedir())
```
