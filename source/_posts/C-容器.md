---
title: C++_容器
top: false
cover: false
toc: true
mathjax: false
date: 2022-06-26 06:36:09
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

# C++ 几种容器的相关介绍

- https://blog.csdn.net/bailang_zhizun/article/details/118938955



# 二维容器的定义方式

- ```c++
  int row=2,col=4;
  vector<vector<int> > v(row);//v为容器的容器，大小为2.
  for(int i=0; i<row; i++)
    v[i].resize(col);//里层容器大小设置为4

- ```c++
  int row=2,col=4;
  vector<string> mat(row, string(col, 0))

