---
layout: page.detail
title: windows指令记录 
tags: windows 运维
categories: 运维
date: 2021-03-17
note: 记录windows指令
---

* TOC
{:toc}

# 指令表格

|平台|功能|指令|
|:---|:---|:---|
|win10|执行策略更改|set-ExecutionPolicy RemoteSigned|
|win10|添加网络路由信息|route add 10.0.0.0 mask 255.0.0.0 网关 -p|
|win10|删除路由信息|route delete 10.0.0.0|
|win10|设置适配器启用或者禁用|netsh interface set interface "【适配器名称】" admin=disabled/enable|
|刷新DNS|ipconfig /flushdns|
|后台运行批处理|if "%1"=="hide" <br/> goto CmdBegin <br/> start mshta vbscript:createobject("wscript.shell").run("""%~0"" hide",0)(window.close)&&exit <br/>:CmdBegin|
|启动虚拟平台|Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform|
|禁用虚拟平台|Disable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform|
