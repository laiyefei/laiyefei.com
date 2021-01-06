---
layout: page.detail
title: github指令记录 
tags: github 运维
categories: 运维
date: 2020-12-24
note: 记录github命令
---

* TOC
{:toc}


# GITHUB 操作命令记录

## PACKAGES

### npm

~~~
发布
------------------------------------------------------------------------
1. 准备ACCESS_TOKEN
2. 登录
    npm login --registry=https://npm.pkg.github.com
    > Username: project-repository-manager
    > Password: 【token】
    > Email: 852800491@qq.com
3. 创建 .npmrc -> registry=https://npm.pkg.github.com/project-repository
4. npm publish
------------------------------------------------------------------------
引用：
------------------------------------------------------------------------
5. 项目：.npmrc -> registry=https://npm.pkg.github.com/project-repository
6. npm install 【项目】
~~~
