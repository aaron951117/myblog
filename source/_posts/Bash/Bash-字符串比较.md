---
title: Bash-字符串比较
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
### 包含子字符串
```bash
#!/bin/bash
#
string='hello world'
sub='hello'

if [[ $string =~ $sub ]]
# if [[ $string = *$sub* ]]
# if [[ $string =~ ^.*$sub.*$ ]] # 正则表达式
then
    echo '包含'
else 
    echo '不包含'
fi
```

### 以某个字符串作为开始
```bash
#!/bin/bash
#
string='hello world'
sub='hello'

if [[ $string = $sub* ]]
#if [[ $string =~ ^$sub.*$ ]] # 正则表达式
then
    echo 'YES'
else 
    echo 'NO'
fi
```

### 以某个字符串作为结束
```bash
#!/bin/bash
#
string='hello world'
sub='world'

if [[ $string = *$sub ]]
#if [[ $string =~ ^.*$sub$ ]] # 正则表达式
then
    echo 'YES'
else 
    echo 'NO'
fi

```