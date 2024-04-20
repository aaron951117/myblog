---
title: git
top: false
cover: false
toc: true
mathjax: false
date: 2022-01-21 02:24:06
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

Git是目前世界上最先进的分布式版本控制系统。
![[Pasted image 20230330173533.png]]
# 使用

## 关于分支

### 删除分支
https://chinese.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/
2020年11月30日
```bash
# 删除本地分支
git branch -d localBranchName
# 删除远程分支
git push origin --delete remoteBranchName
# 删除远程分支
git branch -r -d origin/branch-name  
git push origin :branch-name
# 删除本地分支里远程不存在的分支
git fetch --prune
```

### 切换分支
  - https://chinese.freecodecamp.org/news/git-switch-branch/
  - 2021年4月21日
```bash
# 可以使用它来创建新分支、退出分支、退出特定的 commit 等
git checkout master  # Switched to branch 'master'
git checkout - # switched to last branch
```

### 关联分支
  - https://www.cnblogs.com/bigben0123/p/13208286.html
  - 2020-06-29 15:40
  - https://segmentfault.com/a/1190000039703878
  - 2021-03-24

### 查看分支
```bash
# 加上-a参数可以查看远程分支，远程分支会用红色表示出来（如果你开了颜色支持的话）
git branch -a
# 查看本地分支和远程分支的关联
三选一
git branch -vv
git remote show origin
cat .git/config
```


## 关于仓库
### 仓库地址
```bash
git remote -v
```


# 代理设置
1. https://gist.github.com/laispace/666dd7b27e9116faece6


# git checkout

## 新建分支
```bash
# 本地会新建一个分支名叫 branch_name ，会自动跟踪远程的同名分支 branch_name
# 远程新建了一个分支，本地没有该分支
git checkout --track origin/branch_name
# 本地新建了一个分支 branch_name，但是在远程没有
git push --set-upstream origin new_branch_name  # 在远程新建分支

```
## 切换分支
```bash
git checkout branch_name
```

## 查看git的配置信息
```bash
https://www.cnblogs.com/merray/p/6006411.html
```


# 第一次克隆
1. 需要在机器上生成密钥，然后在网页的git账户上的ssh_key上添加上.pub里的内容
2. 不要在需要sudo的目录下克隆，需要在root的.ssh文件夹也生成密钥，在网页传入账户的ssh_key

# 生成公钥
1.
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@domain.com"
ssh-keygen -t rsa -C "your_email@qq.com"
```

