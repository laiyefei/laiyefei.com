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
~~~

## GIT 以镜像方式推送

~~~
git push --mirror 【GIT仓库地址】
~~~
