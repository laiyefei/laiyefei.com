---
layout: page.detail
title: maven 常见问题
tags: maven 问题
categories: 问题
date: 2020-12-12
note: 记录maven的常见问题
---

* TOC
{:toc}


# MAVEN 常见问题

~~~
1. maven 使用github资源
    1.1. add in pom.xml
    <repositories>
        <repository>
            <id>aliyun-repository</id>
            <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
        </repository>
        <repository>
            <id>project-repository</id>
            <url>https://maven.pkg.github.com/project-repository/repo-mvn</url>
        </repository>
    </repositories>
    1.2. add to settings.xml
    <servers>
        <server>
            <id>【你的自定义 id】</id>
            <username>【你的 github 账号】</username>
            <password>【你的 github token】</password>
        </server>
    </servers>
2. maven 使用本地jar包
    2.1. 
        <dependency>
          <groupId>【groupId】</groupId>
          <artifactId>【artifactId】</artifactId>
          <version>【version】</version>
          <scope>system</scope>
          <systemPath>${project.basedir}/lib/【jar包名称】</systemPath>
        </dependency>
~~~
