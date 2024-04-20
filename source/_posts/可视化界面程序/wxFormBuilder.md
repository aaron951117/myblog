---
title: wxFormBuilder
top: false
cover: false
toc: true
mathjax: false
date: 2023-06-08 10:19:52
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# 设计步骤
1. Forms ---> 添加Frame（框体）
2. 给窗体添加布局器BoxSizer（加上这个才能添加控件）


# 注意事项
1. 如果使用AUI Manager 编译需要指定aui库 -lwx_osx_cocoau_aui-3.2.0(mac) 或者 -lwx_gtk2u_aui-3.0(ubuntu)
2. 使用 PropGrid 组件需要指定库-lwx_osx_cocoau_propgrid-3.2 或者 -lwx_gtk2u_propgrid-3.0

一定不要忘记组合Sizer，从而达到更复杂的布局效果。