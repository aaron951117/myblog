---
title: FTP
top: false
cover: false
toc: true
mathjax: false
date: 2024-03-18 15:09:08
author: TianShan
img: 
coverImg: 
password: 
summary: 
tags: 
categories:
---
# SFTP
命令：
1. 上传本地文件到服务器
```bash
sftp username@remote_server
put /path/to/local_file.txt
put /path/to/local_file.txt /remote/directory
put -r /path/to/local/directory
exit
```
2. 下载服务器文件到本地
```bash
sftp username@remote_server
get file.txt
get file.txt /path/to/local/directory
get -r remote_folder
exit
```
