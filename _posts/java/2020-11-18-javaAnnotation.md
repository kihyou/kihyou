---
layout: post
title: "3. Java注释和注解"
date: 2020-11-18
category: Java
---
单行注释
//注释内容
多行注释
/*
*第一行注释内容
*第二行注释内容
*/
对类或方法的注释
/**
*
*
*/
快捷键：alt+shift+j
注解
@Test
添加：
右键项目 ->Build Path ->Configure Build Path -> Add Library -> Junit -> Next -> 选择版本 -> Finish
(右键项目 -> Build Path -> Add Libraries -> 选择版本 -> Finish)
要求：
方法不能有参数
方法不能是静态的
方法一般是public
@Deprected
v.
对…表示极不赞成; 强烈反对;
在Java中凡是使用@Deprecated标志的类，都是不鼓励使用的类，如果使用或者进行重写，程序会发出警告。
@Override
重写
