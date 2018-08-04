---
title: 博客的使用方法
date: 2018-08-02 16:22:19
tag: ways
---
# 站点配置文件 _config.yml
## 基本信息的修改
title: 博客的名称
subtitle: 小标题
description: 描述
keywords: 关键字
author: 作者
language: 语言 （*这里的语言需要和themes的相一致*）
timezone: 时区
## 主题
    thmem: landscape
    landscape为默认主题，可自行下载喜欢的主题
## 部署
```
deploy:
  type: git
  repo: https://([用户名]:[密码])@github.com/[用户名]/[用户名].github.io.git
  branch: master
```
如需部署在多个服务器上
```deploy:
- type: git
  repo: https://([用户名]:[密码])@github.com/[用户名]/[用户名].github.io.git
- type: git
  repo: XXXX
  branch: master
```
# 主题配置文件 /themes/_config.yml
## 修改头像（本文的主题是nextT,可从网上下载
找到 avatar ，修改头像的url
头像的图片放在 /themes/source/images 文件目录中
## 侧边栏
找到 sidebar 的display属性，里面有四种显示模式，可根据自己喜好选择
post:默认显示方式；
always:一直显示
hide:初始隐藏
remove:移除侧边栏
## 添加菜单选项
一开始，菜单栏只有首页和归档两个选项，在next的主题配置文件中，还有分类，标签，关于。
在配置文件中，找到menu属性，去掉categories,tags,about的注释，
然后在Hexo的根目录执行以下指令
`hexo new page "categories"`  //添加分类页面
`hexo new page "tags"`        //添加标签页面
`hexo new page "about"`       //添加关于页面
在执行完以上指令后，hexo的根目录下的source文件夹会创建三个文件夹，命名分别为：categories,tags,about;
在这些文件夹里面会创建一个以index命名的markdown文件，对这三个markdown文件内容进行修改，分别为：
```
---
title: categories
date: 2018-08-03 22:15:30
type: "categories"
---
---
title: tags
date: 2018-08-03 22:15:30
type: "tags"
---
---
title: about
date: 2018-08-03 22:15:30
type: "about"
---
```
完成修改后，部署hexo便能看到新添加的菜单选项。
## 设置预览
在设置之前，博客里的每篇文章都是显示文章的全部内容，这让人看起来很不舒服是吧？
所以我们就需要把每篇文章都设置成预览模式，这样方便我们查看列表。
在文件中找到auto_excerpt属性，将enable设置为true就可以了，同时你还可以设置length控制预览的字数