---
layout: page.detail
title: python 命令记录
tags: python 运维
categories: 运维
date: 2020-12-19
note: 记录遇到的一些python指令
---

* TOC
{:toc}


# 升级版本

~~~
1. rm /usr/bin/python
2. ln -s /usr/bin/python3 /usr/bin/python
3. rm /usr/bin/pip
4. ln -s /usr/bin/pip3 /usr/bin/pip
~~~

# 安装shadowsocks

~~~
1. shadowsocks.json
    {
        "server":"server.feels.tech",
        "server_port": 10627,
        "local_port": 1080,
        "password":"leaffly",
        "timeout":600,
        "method":"aes-256-cfb"
    }
2. 
    前台：ssserver -c /laiyefei/application/ss/shadowsocks.json
    后台启动：ssserver -c /laiyefei/application/ss/shadowsocks.json --user root -d start
    后台停止：ssserver -c /laiyefei/application/ss/shadowsocks.json --user root -d stop
~~~