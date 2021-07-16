---
layout: page.detail
title: 离线安装 之 离线笔记
tags: 笔记 offline
categories: 笔记
date: 2021-07-06
note: 离线安装 之 离线笔记记录
---

* TOC
{:toc}

# 小技巧记录

~~~
1. 整体依赖包下载
    1.1. 利用yum打包依赖
    	1.1.1. yum 安装工具
        yum -y install yum-utils
        1.1.2. 未下载
        yumdownloader --resolve --destdir=【下载目录】 【应用】
        1.1.3. 已下载
        repoquery -R --resolve --recursive 【应用】 | xargs -r yumdownloader 
2. 
~~~