---
layout: page.detail
title: git指令记录 
tags: git 运维
categories: 运维
date: 2020-12-25
note: 记录git命令
---

* TOC
{:toc}


# GIT 命令记录

## GIT 子模块

~~~
1. 删除git子模块缓存
    git rm -r -f --cached 【子模块路径】
2. 创建git子模块文件
    fsutil file createnew ./.gitmodules 0
3. 添加git子模块
    git submodule add 【git地址】 【子模块路径】
4. 拉取全部
    git clone --recursive 【git地址】
5. 强制覆盖本地
    git fetch --all
    git reset --hard 【分支】
6. git子模块更新
    git submodule update --init --recursive
7. 拉取所有子模块
    git submodule foreach git reset --hard 【分支】
    git pull --recurse-submodules    
~~~

## GIT 以镜像方式推送

~~~
git push --mirror 【GIT仓库地址】
~~~
