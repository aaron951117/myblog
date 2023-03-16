---
title: GAN
top: false
cover: false
toc: true
mathjax: false
date: 2022-08-05 18:43:16
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

# B站1

视频链接：https://www.bilibili.com/video/BV1xm4y1X7KZ?spm_id_from=333.337.search-card.all.click&vd_source=dddc91392492f646c0ba2f2df3838f28

## GAN原理

- GAN设计的关键在于损失函数的处理
- GAN结构的精妙之处在于对生成模型损失函数的处理
- 判别器同时接收生成器生成的图片和真实图片，判别器的目标是尽量将生成的图片和真实的图片区分开
- 在计算过程中能否正确区分生成的图片和真实的图片将作为判别器的损失，能否生成近似真实的图片并使得判别器将生成的图片判定为真将作为生成器的损失
