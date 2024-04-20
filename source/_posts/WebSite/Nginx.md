---
title: nginx
top: false
cover: false
toc: true
mathjax: false
date: 2023-05-05 16:24:49
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# 重载和重启
1. 重载 sudo nginx -s reload
2. sudo nginx -t -c /etc/nginx/nginx.conf
3. 重启 sudo systemctl restart nginx

# 修改nginx的默认端口
https://blog.csdn.net/YLD10/article/details/80242487


# 访问图片403
1. 权限问题，给图片赋予权限 755

# 美化文件浏览器
https://lanffy.github.io/2017/12/27/Nginx-Browse-Folder-Config


# 编译nginx
https://blog.csdn.net/liuYinXinAll/article/details/88357669

提示 没有安装GD library:
./configure: error: the HTTP image filter module requires the GD library.
You can either do not enable the module or install the libraries.
解决:
sudo apt-get install -y libgd-dev
如果在安装libgd-dev时提示找不到
在 vim /etc/apt/sources.list 中添加一行ubuntu 的镜像源
deb http://security.ubuntu.com/ubuntu trusty-security main
提示 没有 GeoIp library
./configure: error: the GeoIP module requires the GeoIP library.
You can either do not enable the module or install the library.

解决
sudo apt-get install libgeoip-dev

下载网址
http://nginx.org/en/download.html

```
# Nginx configure error: the HTTP rewrite module requires the PCRE library
sudo apt-get install libpcre3-dev

# Nginx – ./configure: error: the HTTP XSLT module requires the libxml2/libxslt libraries
sudo apt-get install libxslt-dev
```
