---
title: B站计算机网络和计算机底层原理
top: false
cover: false
toc: true
mathjax: false
date: 2022-08-01 11:25:03
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

# 马士兵

- P1
  - 操作系统找到进程里面要执行的第一句代码
  - 把程序复制到内存里，需要为进程分配资源
- P2
  - 缓存一致性
  - 不同CPU有不同的缓存一致性协议
  - 缓存行64个字节
  - long类型 8个字节
- P4
  - DCL double check lock()双层检查锁
- P5
  - 上锁的代码保证原子性，可见性
  - 程序优化：CPU级别优化，编译器级别优化
    - 线程调度算法CFS（completely fair strategy）综合考虑优先级以及等待时间的算法
