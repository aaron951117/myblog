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

# 迭代容器
```c/c++
#include"MyCout.h"

void MyPrint_3_Dimension_Vector(vector<vector<vector<double>>> Three_Dimension_Vector)
{
	int i = 0;
	for (vector<vector<vector<double>>>::iterator it = Three_Dimension_Vector.begin(); it != Three_Dimension_Vector.end(); it++)
	{
		cout << ++i << endl;
		for (vector<vector<double>>::iterator itt = (*it).begin(); itt != (*it).end(); itt++)
		{
			for (vector<double> ::iterator t = (*itt).begin(); t != (*itt).end(); t++)
			{
				cout << (*t) << " ";


			}cout << endl;
		}
	}
}
```
