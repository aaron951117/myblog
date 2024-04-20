---
title: Bash-字符串操作
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

提取字符串中的数字
```bash
echo hgdfjg678gfdg kjg45nn | tr -d -c 0-9 # 输出 67845
```

```bash
temp = `echo "helloworld20181212 | tr -cd "[0-9]""` 
echo ${temp}
# helloworld
```

 https://blog.csdn.net/dongwuming/article/details/50605911


# 字符串截取
http://c.biancheng.net/view/1120.html
https://wangdoc.com/bash/string
```bash
#!/bin/bash

url="http://c.biancheng.net/index.html"
echo ${url#*/}    #结果为 /c.biancheng.net/index.html
echo ${url##*/}   #结果为 index.html

str="---aa+++aa@@@"
echo ${str#*aa}   #结果为 +++aa@@@
echo ${str##*aa}  #结果为 @@@
```

```bash
#!/bin/bash

url="http://c.biancheng.net/index.html"
echo ${url%/*}  #结果为 http://c.biancheng.net
echo ${url%%/*}  #结果为 http:

str="---aa+++aa@@@"
echo ${str%aa*}  #结果为 ---aa+++
echo ${str%%aa*}  #结果为 ---
```
