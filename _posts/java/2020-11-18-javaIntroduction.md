---
layout: post
title: "1. Java介绍"
date: 2020-11-18
category: Java
---
## JAVA特点
简单性：语法规范，形式简单易学
健壮性：强大的异常处理机制
安全性：沙箱模型，提供安全机制
跨平台：可以一次编写，在不同操作系统平台上运行
## JAVA开发三步
### 1.开发
进行代码的编写
```java
public class hw{
  public static void main(String args[]){
      System.out.println("hello world!");
  }
}
```

### 2.编译
使用DOS命令  
`cd /d D:`——进入d盘  
`cd 文件夹名`——进入文件夹  
`javac 文件名.java`——编译命令，会生成.class字节码文件

### 3.运行
dos命令：  
`java 文件名.class`

## 常用命令
```java
javac 文件名.java        ——编译.Java文件
java 文件名            ——运行.class文件（类文件）
java -jar 文件名.jar    ——运行.jar文件
javaw 文件名.jar        ——运行swing程序
javah                    ——生成c语言头文件
```
