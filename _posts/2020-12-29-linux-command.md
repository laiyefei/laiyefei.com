---
layout: page.detail
title: linux指令记录 
tags: linux 运维
categories: 运维
date: 2020-12-29
note: 记录linux指令
---

* TOC
{:toc}


# 指令表格

|功能|指令|
|:---|:---|
|查看操作系统版本|uname -a|
|查看系统资源情况|top|
|创建用户|useradd laiyefei|
|设置密码|passwd laiyefei|
|编辑超管文件|vi /etc/sudoers|
|给文件夹授权|chown -R 用户:用户 /【文件夹】 |
|查看用户分组信息|groups|
|找到进程并关闭|ps -ef \| grep cloud-desktop-v1.0.0-SNAPSHOT.jar \| awk '{print $2}' \| xargs kill -9|