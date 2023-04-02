---
title: python时间模块
top: false
cover: false
toc: true
mathjax: false
date: 2022-02-25 17:57:58
author:
img:
coverImg:
password:
summary:
tags:
Categories: python
---

# python CST时间转换为其他格式字符串

## 思路: 先把CST格式时间转换为时间对象,在对转换成的时间对象做字符串格式转换

```python
import time
# 实例 CST 格式字符串
timestr = 'Fri Feb 25 17:35:08 CST 2022'
# 转换为 其它时间格式字符串
timestr2 = time.strftime('%Y%m%d_%H%M%S', time.strptime(timestr, '%a %b %d %H:%M:%S CST %Y'))
print(timestr2)
```

