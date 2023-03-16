---
title: Bash-数组
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

1. 遍历列表值
```bash
for i in ${a[*]}; 
do  
	echo ”$i“
done
```

2. 数组
```bash
### Shell 数组元素个数
${#array[@]}
###数组的所有元素
${array[*]}
###字符串长度
${#str}
### 数组结尾添加元素
array[${#array[@]}]=element
```
