---
layout: post
title: "2. Java环境搭建"
date: 2020-11-18
category: Java
---
### 1.JDK  
JDK的安装  
网址：  
https://www.oracle.com/technetwork/java/javase/downloads/index.html  
JDK目录介绍  
bin——JDK包含的一些开发工具执行文件  
lib——Java开发工具要用的一些库文件  
jre——JDK使用的Java运行环境（JRE）的根目录，这个运行环境实现了Java平台  
### 2.环境变量  
计算机-右键-属性-高级系统设置-高级-环境变量  
创建3个系统变量：  
JAVA_HOME : JDK安装主路径  
path: `%JAVA_HOME%\bin`  
classpath：`.;%JAVA_HOME%\lib\tools.jar;%JAVA_HOME%\jre\lib\rt.jar;`  
通过cmd.exe运行java，javac命令检测环境变量配置是否成功  
### · 集成式开发平台  
#### 1. Eclipse  
可扩展开发平台  
一个框架和一组服务  
通过插件组件构建开发环境  
附带一个标准的插件集（包括JavaSE开发工具）  
开放源代码  
基于Java  
#### 2. MyEclipse  
企业级集成开发环境  
在eclipse的基础上加上自己的插件开发而成  
功能强大  
自带javaEE开发工具和jdk  
#### 3. IntelliJ IDEA  
JetBrains公司的产品  
免费版只支持Java等少数语言  
旗舰版还支持HTML, CSS, PHP, MySQL, Python等  
#### 4. Android Studio  
Android开发环境  
基于IntelliJ IDEA.  
类似于Eclipse ADT  
提供了集成的Android开发工具用于开发和调试  
### · myeclipse安装  
myeclipse版本：MyEclipse CI 2019.4  
win下载地址：  
https://pan.baidu.com/share/init?surl=0bpqJP9MnSv2wBdqcuHRcA  
提取码：7xdi  
破解工具：https://pan.baidu.com/s/1953feWjM8p67LGl_lLu9fg  
提取码：o3d8  
破解教程：https://blog.csdn.net/woxiaohousheng/article/details/81560916  
各平台：https://my.oschina.net/u/1381027/blog/3055081  
### · Eclipse的使用  
#### 1. 项目结构  
工作空间（workspace，内部项目间调用）  
项目（project, 导入导出编译，添加jar库文件）  
包（package、import、常用包）  
#### 文件目录结构  
##### src：  
源码文件夹，存放编译前的源代码  
##### bin：  
工程输出路径，存放编译后的.class字节码文件  
##### .classpath和.project  
工程描述文件  
#### 2. 重新配置JDK  
Window-Preferences-Java-Installed JREs  
#### 3. 统一编码格式UTF-8  
##### eclipse中修改编码格式：  
Window->Preferences->General：  
Editors->Text Editor->Spelling->Encoding  
Workspace->Text file encoding  
##### 工程（Project）：  
Properties-Resource->Text file encoding  
##### 文件：  
Properties-Resource->Text file encoding  
