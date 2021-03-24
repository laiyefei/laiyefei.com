---
layout: page.detail
title: git 常见问题
tags: git 问题
categories: 问题
date: 2020-12-15
note: 记录git的常见问题
---

* TOC
{:toc}


# 问题配置

~~~
1. 文件太长
    git config --global core.longpaths true
2. LF will be replaced by CRLF
    git config --global core.autocrlf false
3. 删除文件历史提交记录
    git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch 【文件相对地址】' --prune-empty --tag-name-filter cat -- --all
    git push origin --force --all
    git push origin --force --tags
    git for-each-ref --format='delete %(refname)' refs/original | git update-ref --stdin
    git reflog expire --expire=now --all
    git gc --prune=now
4. 权限不够
    git update-index --chmod=+x [文件名]
5. 文件大小限制
    git config http.postBuffer 524288000 （52428000=500×1024×1024,即500M）
6. 上传大文件
    git lfs install 
    git lfs track
~~~
