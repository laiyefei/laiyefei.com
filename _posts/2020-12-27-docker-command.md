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
|启动所有容器|docker start $(docker ps -a \| awk '{ print $1}' \| tail -n +2)|
|运行指定宿主机端口:容器端口|docker run -d -p 【宿主机端口】: 【容器端口】|
|将镜像存为本地文件|docker save -o 【镜像文件名.docker】 【id】|
|加载镜像文件|docker load -i 【镜像文件】|
|删除某个tag|docker rmi 【镜像名】|


# 常见问题

~~~
1. 安装仓库
    docker run -d -p 5000:5000 --restart=always --name registry registry
2. docker push 报错 http: server gave HTTP response to HTTPS client
    源docker
    vim /etc/docker/daemon.json
    { 
        "insecure-registries":[
            "registry.laiyefei.com:9998"
        ] 
    }
3. 从本地仓拉镜像
    3.1. vim /usr/lib/systemd/system/docker.service 
    3.2. --add-registry=127.0.0.1:9998  --insecure-registry=127.0.0.1:9998 \  【加在ExecStart=第一行】

~~~



# 安装软件复杂指令备忘录

~~~
1. yearning
    docker run -d -it -p8000:8000 -e MYSQL_USER=root -e MYSQL_ADDR=yearning.laiyefei.com:3306 -e MYSQL_PASSWORD=123123 -e MYSQL_DB=Yearning
    
2. 
~~~