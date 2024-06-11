---
title: QT问题
top: false
cover: false
toc: true
mathjax: false
date: 2024-03-13 21:56:18
author: TianShan
img: 
coverImg: 
password: 
summary: 
tags: 
categories:
---
2024-03-13 21:56:28
1. 为什么utils包含了头文件#include "mainwindow.h"还需要声明类class MainWindow;
8U3eUt8U3eUt
2. 过滤小工具在读取了新文件之后使用clear清除了表格里的内容，又重新新建了对象，那么之前的对象没有delete会不会存在内存泄漏。


qmake -tp vc

# G++ 编译QT
g++ -std=c++11 -o my_program my_program.cpp `pkg-config --cflags --libs Qt5Core` -fPIC
