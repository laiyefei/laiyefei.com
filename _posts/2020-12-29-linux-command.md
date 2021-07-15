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
|查看操作系统版本|cat /etc/redhat-release|
|查看系统资源情况|top|
|创建用户|useradd laiyefei|
|查看用户|cat /etc/passwd|
|查看用户组|cat /etc/group|
|查看当前活动用户|w|
|设置密码|passwd laiyefei|
|编辑超管文件|vi /etc/sudoers|
|给文件夹授权|chown -R 用户:用户 /【文件夹】 |
|查看用户分组信息|groups|
|找到进程并关闭|ps -ef \| grep 【进程名】 \| grep -v grep \| awk '{print $2}' \| xargs -r kill -9|
|拷贝强行覆盖文件|\cp -rf  【源文件】 【目标文件夹】|
|创建软连接|ln -s 【源文件】 【目标文件】|
|列出所有服务列表|systemctl list-unit-files|
|列出可用服务列表|systemctl list-units|
|查CPU核心数|cat /proc/cpuinfo\| grep "physical id"\| sort\| uniq\| wc -l


# 常见问题

~~~
1. 如何开机启动
   脚本写入其中 /etc/rc.d/rc.local 
   授权 chmod +x /etc/rc.d/rc.local
2. 
~~~