---
layout: page.detail
title: 离线安装 之 ARTIFACTORY 安装笔记
tags: 笔记 offline 运维
categories: 笔记
date: 2021-07-08
note: 离线安装 之 ARTIFACTORY 安装笔记
---

* TOC
{:toc}


# 准备资源

## 造资源【找一台外网连接的linux系统】

~~~
1. 下载加yum源
    sudo wget https://bintray.com/jfrog/artifactory-rpms/rpm -O /etc/yum.repos.d/bintray-jfrog-artifactory-oss-rpms.repo
2. 下载整体依赖
    yumdownloader --resolve jfrog-artifactory-oss
~~~

ps. 【RPM包较大，不保存】

# 安装命令

~~~
1. rpm -ivh jfrog-artifactory-oss-6.23.23.rpm

2. 附加配置yaml
    1.1. 产生自定义yaml文件
        cat <<EOF>system.yaml
        configVersion: 1
        shared:
            extraJavaOpts: "-server -Xms512m -Xmx2g -Xss256k -XX:+UseG1GC"
            security:
            node:
            database:
        EOF
    1.2. 附加yaml文件到指定yaml文件
        sudo cp -brvf system.yaml /var/opt/jfrog/artifactory/etc/system.yaml
        
3. enable artifactory.service 同时启动
    sudo systemctl enable --now artifactory

4. 启动
    sudo systemctl start artifactory
~~~

# 备注信息

~~~
操作系统版本： CentOS Linux release 7.6.1810 (Core)
~~~