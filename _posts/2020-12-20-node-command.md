---
layout: page.detail
title: node 命令记录
tags: node 运维
categories: 运维
date: 2020-12-20
note: 记录遇见的node命令
---

* TOC
{:toc}


# 项目构建

## gradle + yarn + react + typescript

~~~
1. 安装react脚手架，yarn管理工具
    npm install create-react-app yarn -g

2. 查看脚手架版本，确认安装成功
    create-react-app --version

3. react脚手架创建项目 -> typescript
    create-react-app 【项目】 --typescript
~~~

# 依赖添加

~~~
1. 添加 typescript 支持 
    yarn add typescript -D
~~~

# 配置静态服务器

~~~
yarn init
yarn add @types/node --save-d
yarn add ts-node --save-d
yarn add typescript --save-d
yarn add nodemon -g
yarn add babel-core
yarn add babel-preset-env 
yarn add babel-cli -g
~~~

# 常见指令

~~~
1. yarn
创建项目：yarn init
安装依赖包：yarn == yarn install
添加依赖包：yarn add
配置淘宝镜像：yarn config set registry "https://registry.npm.taobao.org"
查看源: yarn config get registry
命令	                            操作        	            参数	                    标签
yarn add           	            添加依赖包	            包名	                    --dev/-D
yarn bin           	            显示yarn安装目录	        无	                    无
yarn cache       	            显示缓存	                列出缓存包：ls，
                                                        打出缓存目录路径：dir，
                                                        清除缓存：clean	        无
yarn check       	            检查包	 	 
yarn clean       	            清理不需要的依赖文件	 	 
yarn config                     配置	                    设置：set <key> <value>， 
                                                        删除：delete， 
                                                        列出：list	[-g | --global]
yarn generate -lock-entry	    生成锁定文件	            无	                    无
yarn global                     全局安装依赖包	            yarn global 
                                                        <add/bin/list/
                                                        remove/upgrade> 
                                                        [--prefix]	            --prefix 包路径前缀
yarn info         	            显示依赖包的信息	        包名	                    --json：json格式显示结果
yarn init         	            互动式创建/
                                更新package.json文件	    无	                    --yes/-y：以默认值生成package.json文件
yarn install                    安装所有依赖包	 	                                --flat：只安装一个版本；
                                                                                --force：强制重新下载安装；
                                                                                --har：输出安装时网络性能日志；
                                                                                --no-lockfile：不生成yarn.lock文件；
                                                                                --production：生产模式安装（不安装devDependencies中的依赖）
yarn licenses                   列出已安装依赖包的证书	    ls：证书列表；
                                                        generate-disclaimer：
                                                        生成免责声明	 
yarn link         	            开发时链接依赖包，
                                以便在其他项目中使用	    包名	 
yarn login       	            保存你的用户名、邮箱	 	 
yarn logout                     删除你的用户名、邮箱	 	 
yarn list         	            列出已安装依赖包	 	                            --depth=0：列表深度，从0开始
yarn outdated                   检查过时的依赖包	        包名	 
yarn owner       	            管理拥有者	            ls/add/remove	 
yarn pack         	            给包的依赖打包	            --filename	 
yarn publish                    将包发布到npm	 	                                --tag：版本标签；
                                                                                --access：公开（public）
                                                                                还是限制的（restricted）
yarn remove                     卸载包，更新package.json
                                和yarn.lock	            包名	 
yarn run           	            运行package.json中
                                预定义的脚本	 	 
yarn self -update           	yarn自身更新--未实现	 	 
yarn tag           	            显示包的标签	            add/rm/ls	 
yarn team         	            管理团队	                create/destroy
                                                        /add/rm/ls	 
yarn test         	            测试 = yarn run test	 	 
yarn unlink                     取消链接依赖包	 	 
yarn upgrade                    升级依赖包	 	 
yarn version                    管理当前项目的版本号	                            --new-version ：直接记录版本号；
                                                                                --no-git-tag-version：不生成git标签	 
yarn why           	            分析为什么需要安装依赖包	包名/包目录/包目录中的文件名	 
------------------------------------------------------------------------------------------------------------------------
~~~