---
title: 简易Web用户管理系统
date: 2019.01.06
tag: exercise
categories: 
- blog
---

如何运用angular+go+postgresql实现简易的web用户管理系统
<!-- more -->
# 准备工作
## 安装angular
+ 前提条件：你的开发环境已经包含[Node.js](https://nodejs.org/en/)和[npm包管理器](https://docs.npmjs.com/about-npm/index.html)
### step1:安装Angular CLI
打开终端/控制台窗口，并输入以下命令：

`npm install -g @angular/cli`

然后经历过漫长的等待之后……
+ 需要注意的是，在npm install的时候需翻墙，若不翻墙会导致某些组件无法成功安装，出现Error警告字样。


---
### step2:创建工作空间和初始应用
1.运行CLI命令ng new，并提供一个名字my-app

`ng new my-app`

该行命令则表示创建一个名为my-app的应用。因为Angular CLI 会安装必要的Angular npm包及其他依赖，所以这里可能也要花上一些时间。
该命令还会创建下列工作空间和初始项目文件：
+ 一个新的工作空间，根目录名为my-app
+ 一个初始的骨架应用项目，也叫my-app（位于src目录下）
+ 一个端到端的测试项目（位于e2e目录下）
+ 相关的配置文件

---
### step3:启动服务器
1.首先进入工作空间目录（my-app）
2.使用CLI明明令ng serve 启动开发服务器，并带上 --open选项

`
cd my-app
ng serve --open
`

选项中的--open可简化为-o，具体可参考-help选项。

---
### step4:安装成功啦
当出现下面这个图，代表你已经成功安装angular cli啦

![](https://angular.cn/generated/images/guide/cli-quickstart/app-works.png)


## 安装go
## 安装postgresal
