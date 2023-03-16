---
title: docker使用
top: false
cover: false
toc: true
mathjax: false
date: 2022-03-20 14:37:28
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

# 3090服务器的镜像名称版本信息

- gcn v1 
  ssh登陆服务
  git服务

# 关于容器网络

运行的容器端口映射到宿主机端口 方法： 先保存为镜像 再开启镜像
参考 https://blog.csdn.net/nienelong3319/article/details/106796519

# 容器镜像操作

https://www.cnblogs.com/kevingrace/p/9599988.html

# 关于容器磁盘
查看容器镜像和容器所占空间 sudo docker system df

# linux 网络通信
lsof -i:端口号  可以查看端口号对应的服务是否开启
netstat -ap 查看所有开启的端口号
ss -tunlp 查看所有开启的端口号

# 远程连接 jupyter-lab
https://blog.csdn.net/GouGe_CSDN/article/details/104567559
https://www.cnblogs.com/wangzi199/p/13352475.html
https://blog.csdn.net/eswai/article/details/79437428

# pycharm jetbrain远程连接 docker

## 方法有两种 1.docker开启ssh 2.通过tcp直接访问docker服务

https://blog.csdn.net/thanours/article/details/109271836
https://www.freesion.com/article/85511409241/
https://www.jianshu.com/p/f6e02bfc18b4
https://www.thisfaner.com/p/configure-docker-in-intellij-idea/

# jupyter-lab 虚拟环境
https://www.cnblogs.com/2696ww/p/14685434.html

# 遇到的问题
密码正确但是ssh连接permission deny https://www.cnblogs.com/sunzebo/articles/9609457.html
查看ip
docker inspect container_name | grep IPAddress

- 登录不上去 使用 passwd 更改一下密码

# 创建容器命令：
容器执行代码
sudo docker run -it --name onlyGraph3 -p 1022:22 -v /home/tianshan/WorkSpace/_share:/home/workspace/_share --shm-size=2g --gpus all onlygraph:v2

远程pycharm调试代码
创建容器命令注释
sudo docker run -it --name Graph \  # 容器命名
-p 1022:22 \  # ssh 端口
-p 1088:8888 \  # jupyter 端口
-v /home/tianshan/WorkSpace/_share/GCN/data:/tmp/data \
-v /home/tianshan/WorkSpace/_share/GCN/experiment:/tmp/experiment \
-v /home/tianshan/WorkSpace/_share:/home/workspace/_share \
--shm-size=2g --gpus all onlygraph:v2



sudo docker run -it --name gcn0 \
-p 10022:22 \
-p 10020:50020 \
-p 10021:21 \
-p 1088:8888 \
-v /etc/timezone:/etc/timezone \
-v /etc/localtime:/etc/localtime \
-v /home/tianshan/WorkSpace/_share/docker0_tmp:/tmp \
-v /home/tianshan/WorkSpace/_share/paper_01_souce_code/data:/tmp/data \
-v /home/tianshan/WorkSpace/_share/paper_01_souce_code/experiment:/tmp/experiment \
-v /home/tianshan/WorkSpace/_share:/home/workspace/_share \
--shm-size=2g --gpus all gcn:v5



# 从镜像创建容器

sudo docker run -d  --name container_name -it image_name /bin/bash 

sudo docker run -d  --name container_name  --net host  --gpus all -it image_name /bin/bash 

sudo docker run -d  --name nasg02  --net host  --cpus 4 --shm-size=32G --gpus all -it ubuntu /bin/bash 

sudo docker run -d  --name nasg02  --net host  --shm-size=32G --gpus all -it 【ubuntu】 /bin/bash \

-v /home/tianshan/WorkSpace/_share/docker_nasg_tmp:/tmp \



- --net host 与宿主机端口保持一致
- -p 宿主机端口:docker端口
- --gpus all 对docker可见gpu



# 查看docker内存

cat /proc/meminfo





# 如何优雅的退出容器

按“Ctrl+P+Q”按钮退出容器，即可正常退出不关闭容器

# 删除容器
docker rm 容器名

python main.py --train_epoch=50
没有试过的方法：
给运行中的容器修改 /dev/shm 大小 https://blog.csdn.net/iteye_4064/article/details/82679418



# 关于bash

- 无法使用上下键切换指令
  https://www.cnblogs.com/maohedashu/p/13494907.html

# 用户登录

- 创建非root用户登录
  https://segmentfault.com/a/1190000040466843
  https://keykernel.org/2018/05/13/docker-run-in-user/



# 容器使用宿主机的代理配置

- https://kebingzao.com/2019/02/22/docker-container-proxy/
