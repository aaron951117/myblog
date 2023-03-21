---
title: Bash-if 判断符号
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

-eq       //等于  
-ne       //不等于  
-gt        //大于 （greater）  
-lt         //小于 （less）  
-ge       //大于等于  
-le        //小于等于


逻辑与：    &&  
第一个条件为假时，第二个条件不用再判断，最终结果已经有；  
第一个条件为真时，第二个条件必须得判断。  
逻辑或：    ||  
逻辑非:       !


1. shell中如果是等于、不等于，既可以用 -eq、-ne （外面需要加中括号），也可以用 == 、!=（外面加中括号或双括号都行）
2. shell中如果是大于，大于等于，小于，小于等于，用 -gt, -ge,-lt,-le 的话，则需要加中括号
3. **shell中大于、大于等于，小于，小于等于想用 >,>=,<,<=，则需要加双括号，而不是中括号**