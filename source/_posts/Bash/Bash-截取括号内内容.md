---
title: Bash-截取括号内内容
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

1. 使用grep（结果带括号，不知道有没有办法仅把括号中的内容匹配出来）
```bash
$a='abc[edg]adfirpqu'
$echo $a|grep -o '\[.*\]' #中括号的处理需要转义
[edg]
    

$b='abc(edg)adfirpqu'
$echo $b|grep -o '(.*)'
 (edg)
```

2.  使用cut
```bash
$a='abc[edg]adfirpqu'
$echo $a|cut -d '[' -f2|cut -d ']' -f1
edg
    

$b='abc(edg)adfirpqu'
$echo $a|cut -d '(' -f2|cut -d ')' -f1
edg
```

3. 使用字符串截取
```bash
$a='abc[edg]adfjaierqpwe'
$b=${a#*[}
$echo $b
edg]adfjaierqpwe`


$c=${b%]*}
$echo $c
edg
```