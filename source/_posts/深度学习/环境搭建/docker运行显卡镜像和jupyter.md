---
title: docker运行显卡镜像和jupyter
top: false
cover: false
toc: true
mathjax: false
date: 2024-03-05 18:22:09
author: TianShan
img: 
coverImg: 
password: 
summary: 
tags: 
categories:
---
# 运行docker并端口映射到宿主机
```bash
sudo nvidia-docker run -it -p 7777:8888 --ipc=host -v /home/lab/Documents/iris_workspace:/iris_workspace --gpus all --shm-size 16G --name iris_notebook  cf60a305ba7b
```
- -it：为直接进入交互式 ；
- -p 7777:8888：是把主机的7777端口映射到容器的8888端口；
- -ipc=host：可以让容器与主机共享内存 ；
- --name xxxxx：给容器定义一个个性化名字
- -v /home/lab/Documents/iris_workspace:/iris_workspace：指示docker挂载目录，以便可以在容器环境内部进行访问。如果您有数据集或代码文件，请将它们设置为可在特定目录上使用，并通过此选项进行挂载。可以将主机上的 /home/lab/Documents/iris_workspace 地址挂载到容器里，并命名为/iris_workspace，这样这个文件夹的内容可以在容器和主机之间共享了。**那么在容器内进入/**iris_workspace**目录，便可访问到我硬盘内** /home/lab/Documents/iris_workspace **文件夹下的内容**。因为容器一旦关闭，容器中的所有改动都会清除，所以这样挂载一个地址可以吧容器内的数据保存到本地。
- --shm-size 16G ：默认分配很小的内参，在训练模型时不够用，可以通过参数设置
- --gpus all：默认是不把GPU加入到docker环境中的，但可以通过参数设置
- - cf60a305ba7b：是你安装的**jupyter镜像的id**，可以在刚刚docker images命令后面查看，当然你也可以直接写全名ufoym/deepo:all-py36-jupyter
- nvidia-docker：否则在镜像中无法使用gpu