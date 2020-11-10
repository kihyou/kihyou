---
layout: post
title: "使用GitHub Pages + Jekyll + Atom 搭建个人博客（win10）"
date: 2020-11-09
category: Jekyll
---
## 一、GitHub

### 1. 注册
### 2. 创建仓库并开启GitHub Pages  
  按教程到第7步：  
  [怎样在github上创建一个github pages的博客](https://jingyan.baidu.com/article/acf728fd64b5a2f8e510a31d.html)

### 3. 仓库克隆到本地
  可以使用GitHub Desktop将仓库克隆到本地。  
  [教程](https://www.jianshu.com/p/06a960d991aa)
## 二、Jekyll

### 1. 安装
### 2. 初始化仓库
  1. cmd进入到仓库所在路径，执行以下代码:  
    ```cmd
      jekyll new .
    ```
  2. 拷贝出`Gemfile`和`Gemfile.lock`两个文件备用  

### 3. 选择博客主题下载
  [主题网站](http://jekyllthemes.org/)  
  选择一个主题进行下载，下载后解压到本地仓库
### 3.1 模板修改
  可以参考[Github+Jekyll 搭建个人网站详细教程](https://www.jianshu.com/p/9f71e260925d)中的第四步目录结构，对模板内容选择性地修改。
### 4. 服务启动（本地访问）
  cmd进入仓库路径下，执行以下代码  
  ```cmd
    jekyll server
  ```
  cmd中的`Server address`就是搭建完成后的本地服务地址，在浏览器输入即可进入
  > PS:若下载的主题`jekyll server`执行失败，则用步骤二中拷贝的`Gemfile`和`Gemfile.lock`文件替换下载的主题里面的该文件，若还不成功，则根据控制台提示的错误，可以百度到解决方案。

## 三、Atom —— 编辑器
  [下载地址](https://atom.io/download/windows_x64)  
  [教程](https://www.hangge.com/blog/cache/detail_1149.html)  
  
## 参考
 1. [使用 GitHub Pages](https://docs.github.com/cn/free-pro-team@latest/github/working-with-github-pages)
 2. [Github+Jekyll 搭建个人网站详细教程](https://www.jianshu.com/p/9f71e260925d);
 3. [搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html);
 4. [怎样在github上创建一个github pages的博客](https://jingyan.baidu.com/article/acf728fd64b5a2f8e510a31d.html);
 5. [0基础的git教程，傻瓜都会用的Github Desktop](https://www.jianshu.com/p/06a960d991aa)
 6. [Atom - 介绍和使用方法（好用的文本编辑器，代码提示高亮、Markdown）](https://www.hangge.com/blog/cache/detail_1149.html)
