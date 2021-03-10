---
layout: page.detail
title: nginx笔记
tags: nginx 笔记 中间件
categories: 笔记
date: 2020-12-21
note: 记录遇到的一些nginx问题
---

* TOC
{:toc}


# docker安装

~~~
1. docker pull nginx:latest
2. docker run --name nginx -p 80:80 -d nginx
~~~

# nginx 配置

~~~
1. 转发请求
location /路由 {
    proxy_pass 【目标地址】;
}
2. 转发二级域名
if ($http_host ~* "^(.*?)【域名】$") {
    set $domain $1;
}
location / {
    if ($domain ~* "【关键字】") {
        proxy_pass 【目标地址】;
    }
}
~~~