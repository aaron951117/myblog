---
title: MySQL
top: false
cover: false
toc: true
mathjax: false
date: 2023-05-05 14:31:31
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# MySQL-8.0
```mysql
# MySQL5.7以后，password字段不再存在，变成了authentication_string
SELECT User, Host, authentication_string FROM mysql.user;
# 给某个用户修改密码
ALTER USER 'pig'@'%' IDENTIFIED WITH mysql_native_password BY '1234';
```
