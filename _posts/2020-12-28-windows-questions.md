---
layout: page.detail
title: windows常见问题记录
tags: 运维 windows
categories: 运维
date: 2020-12-28
note: 记录windows下常见问题
---

* TOC
{:toc}


# 常见问题
~~~

~~~


# 安装记录

## 安装SSH服务

### 下载openssh

{% include download.link.md name='OpenSSH-Win32.7z' path='/OpenSSH-Win32.7z' %}

### 输入安装指令

进入当前解压目录：

~~~
powershell.exe -ExecutionPolicy Bypass -File install-sshd.ps1
~~~

### 配置防火墙放行

~~~
netsh advfirewall firewall add rule name=sshd dir=in action=allow protocol=TCP localport=22
~~~

### 启动ssh服务

~~~
net start sshd
~~~