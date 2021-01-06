---
layout: page.detail
title: docker指令记录 
tags: docker 运维
categories: 运维
date: 2020-12-27
note: 记录docker命令
---

* TOC
{:toc}


# 指令表格

|功能|指令|
|:---|:---|
|进入docker容器|docker exec -it [code] /bin/bash|
|构建docker|docker build -t [tag]:v .|
|保存docker镜像|docker save -o [tag].tar [tag]|
