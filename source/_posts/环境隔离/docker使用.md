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

# docker 安装
https://www.cnblogs.com/Can-daydayup/p/16472375.html

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


# 进入正在运行的docker
sudo docker exec -u 0 -it lucid_williams  /bin/bash



docker 工具

上传下载文件
```bash
docker pull svenstaro/miniserve
```

# docker-compose
1. docker-compose -f file.yaml up -d
2. 查看启动log docker logs 容器ID


# docker run 
参考：https://blog.csdn.net/zhong_jay/article/details/108668246
作用：创建一个新的容器并运行一个命令
-a stdin: 指定标准输入输出内容类型，可选 STDIN/STDOUT/STDERR 三项；
-d: 后台运行容器，并返回容器ID；
-i: 以交互模式运行容器，通常与 -t 同时使用；
-P: 随机端口映射，容器内部端口随机映射到主机的端口
-p: 指定端口映射，格式为：主机(宿主)端口:容器端口
-t: 为容器重新分配一个伪输入终端，通常与 -i 同时使用；
--name="nginx-lb": 为容器指定一个名称；
--dns 8.8.8.8: 指定容器使用的DNS服务器，默认和宿主一致；
--dns-search example.com: 指定容器DNS搜索域名，默认和宿主一致；
-h "mars": 指定容器的hostname；
-e username="ritchie": 设置环境变量；
--env-file=[]: 从指定文件读入环境变量；
--cpuset="0-2" or --cpuset="0,1,2": 绑定容器到指定CPU运行；
-m :设置容器使用内存最大值；
--net="bridge": 指定容器的网络连接类型，支持 bridge/host/none/container: 四种类型；
--link=[]: 添加链接到另一个容器；
--expose=[]: 开放一个端口或一组端口；
--volume , -v: 绑定一个卷

# 查看docker创建时的参数
使用runlike
```bash
sudo pip3 install runlike
```
