---
title: 传参
top: false
cover: false
toc: true
mathjax: false
date: 2023-05-31 17:18:09
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# 参数为列表
https://blog.csdn.net/fdipzone/article/details/61220396
```bash
只会输出第一个元素，所以使用regions作为参数传递，只会传递第一个元素。

因此需要把参数写成 “${regions[*]}” 才可以作为数组传递。

arr=$1 应该改成 arr=($1) ，传参的时候传了一组字符串"GZ SH BJ"，但是接收参数的时候需要重新用括号()括起来，让arr变成数组。  
你上面的代码试试echo ${#arr[*]} 个数是1，正确的结果应该是3.
```

```bash
使用${arr[*]}和使用“${arr[*]}”,带不带引号有着不同，如果带引号，就算是空也会传递一个空字符串，如果不带引号，如果列表为空则不传递。
```

# bash无法将字典作为参数传入函数