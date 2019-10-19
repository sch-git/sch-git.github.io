---
title: Git
date: 2019-10-16 22:56:26
tags:
  - 笔记
  - Git
categories:
  - 开发工具
---
## Git简介
Git是一种分布式版本管理系统，目前已经成为开发人员做项目版本管理的首选，非开发人员也可以用Git来做自己的文档版本管理工具
<!-- more -->
## 常用操作
    不知道大家有没有使用git，但是对git命令基本不了解，使用的时候频繁百度，还不敢保证搜索到的就是对的经历。现在机会来了，掌握了以下git命令，就可以轻松应对90%的需求。
**git clone**
    从服务器拉取代码
**git config**
    配置用户名和邮箱
**git branch**
>创建，重命名，查看，删除项目分支，通常用Git做项目开发时，一般都是在开发分支中进行，完成后再合并到主干
```创建分支
    git branch test/0.0
```
    创建一个名为test/0.0的分支，分支名只要不包含特殊字符即可
```重命名分支
    git branch -m test/0.0 test/0.1
```
    如果觉得之前的分支名不合适，可以为新建的分支重命名，重命名分支为test/0.1
```查询分支
    git branch 
```
    通过不带参数的branch命令可以查看当前项目分支列表
```删除分支
    git branch -d test/0.1
```
    可以通过-d命令删除分支
**git checkout**
```切换分支
    git checkout test/0.1
```
    切换到test/0.1分支
```查看文件变动状态
    git status
    // Changes not staged for commit(改动文件未提交到暂存区)
    // Change to be commited(文件已提交到暂存区)
```
```添加文件变动到暂存区
    git add fileName
```
    通过指定文件名fileName可以将文件添加到暂存区，添加所有文件可用git add .
```提交文件变动到版本库
    git commit -m "提交原因"
```
    通过-m参数可以将文件变动提交到版本库，-m参数可以直接再命令行里面输入描述文本
```
   将本地代码改动推送到服务器：git push origin test/0.1 
```
    origin指代当前的git服务器地址
```
    将服务器上的最新代码拉取到本地：git pull origin test/0.1
```
```
    查看版本提交记录：git log
```
```
    为项目标记里程碑：git tag publish/0.1  git push origin publish/0.1
```
    将项目代码做标记并发布
```
    .gitignore:忽略文件
    设置那些文件不需要推送到服务器上，这是一个配置文件
```
---
未完待续
参考文章[Git从入门到放不下](https://mp.weixin.qq.com/s/d7i_4ls0Ru539PpX0yz0UA)