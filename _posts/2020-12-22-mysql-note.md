---
layout: page.detail
title: mysql笔记
tags: mysql 笔记
categories: 笔记
date: 2020-12-22
note: 记录遇到的一些mysql问题
---

* TOC
{:toc}


# 常见问题

~~~
1. 本地登录切换账户密码登录
    1.1. update mysql.user set host = '%' where user = 'root';
    1.2. FLUSH PRIVILEGES;
    1.3. alter user 'root'@'%' identified with mysql_native_password by 'root'; 
   
2. docker 安装
    1.1. docker pull mysql:latest
    1.2. docker run -itd --name mysql-test -p 3306:3306 -e MYSQL_ROOT_PASSWORD=[password] mysql 

3. 无须密码登录
    my.ini 配置 skip-grant-tables 跳过安全校验

4. 创建用户
    CREATE USER  'username'@'%'  IDENTIFIED BY 'password';

5. 授权
    grant all privileges on *.* to 'username'@'%';
~~~