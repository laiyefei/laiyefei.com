---
layout: page.detail
title: bat指令记录 
tags: bat 运维 windows
categories: 运维
date: 2020-12-28
note: 记录windows下bat指令
---

* TOC
{:toc}


# 指令表格

|功能|指令|
|:---|:---|
|刷新DNS|ipconfig /flushdns|
|后台运行批处理|if "%1"=="hide" <br/> goto CmdBegin <br/> start mshta vbscript:createobject("wscript.shell").run("""%~0"" hide",0)(window.close)&&exit <br/>:CmdBegin|
