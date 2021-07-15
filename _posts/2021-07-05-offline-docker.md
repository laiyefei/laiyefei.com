---
layout: page.detail
title: 离线安装 之 docker 安装
tags: 笔记 offline
categories: 笔记
date: 2021-07-05
note: 离线安装 之 docker 安装
---

* TOC
{:toc}


# docker 安装

## 准备资源

{% include download.link.md name='docker' path='/docker.7z' %}


## 安装命令

~~~
1. 安装
    rpm -ivh 【解压目录】/*.rpm
2. 配置环境变量
~~~


# docker-compose 安装

## 准备资源

{% include download.link.md name='docker-compose-Linux-x86_64' path='/docker-compose-Linux-x86_64.7z' %}

## 安装命令

~~~
1. 从github 下载 docker-compose 
	sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

2. 授权
	sudo chmod +x /usr/local/bin/docker-compose

3. 软链
	sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

4. 测试是否安装成功
	docker-compose --version

~~~



# 备注信息

~~~
操作系统版本： CentOS Linux release 7.6.1810 (Core)
~~~