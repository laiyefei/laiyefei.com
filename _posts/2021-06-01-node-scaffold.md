---
layout: page.detail
title: npm 脚手架开发笔记记录
tags: npm 笔记 脚手架
categories: 笔记
date: 2021-06-01
note: npm 脚手架开发笔记记录
---

* TOC
{:toc}

# npm脚手架编写步骤

1.npm init 初始化一个仓库，如 test

2.在 package.json 添加 bin 节点

3.执行 npm link

4.创建js，如 cli.js，顶格写注释

~~~
#!/usr/bin/env node
console.log('cli working!')
~~~

5.安装两个npm模块

~~~
# 用于命令行交互
npm install inquirer
# 用于模板引擎渲染
npm install ejs
~~~

6.编写cli.js

~~~
#!/usr/bin/env node
// 用于命令行交互
const inquirer = require('inquirer')
// 用户获取文件路径
const path = require('path')
// 用于读取写入文件
const fs = require('fs')
// 用于模板引擎渲染
const ejs = require('ejs')

inquirer.prompt([
  {
    type:'input',
    name:'name',
    message: 'Project name?'
  }
])
.then(answers => {
  console.log(answers)
  // 引入path模块，模板目录写绝对路径
  const tmplDir = path.join(__dirname, 'templates')
  // 目标目录:目标执行的目录，一般在cwd目录
  const destDir = process.cwd()
  // 引入fs模块，将模板下面文件全部转换到目标目录
  fs.readdir(tmplDir, (err, files) => {
    if(err) throw err
    files.forEach(file => {
      // 文件的相对路径
      console.log(file) // index.html    style.css
      // 引入ejs模块
      // 通过模板引擎渲染路径对应的文件
      // 第一个参数是文件的绝对路径
      // 第二个参数是模板引擎工作时候的数据上下文
      // 第三个参数是回调函数
      ejs.renderFile(path.join(tmplDir, file), answers, (err, result) => {
        if(err) throw err 
        // 成功的话就是已经渲染过的文件
        console.log(result)
        // 写入文件，目标目录绝对路径，第二个参数是文件内容
        fs.writeFileSync(path.join(destDir, file), result)
      })
    })
  })
})
~~~

7.创建模板文件 在 templates 文件夹中

~~~
index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title><%= name %></title>
</head>
<body>
</body>
</html>
~~~

~~~
style.css

body{
  margin: 0;
  background-color: bisque;
}
~~~
等等