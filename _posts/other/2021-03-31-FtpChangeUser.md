---
layout: post
title:  "FTP服务器自动进入一个用户名，不能转换成其他用户名登录的解决方法"
date:   2021-03-31
category: other
---
解决方法：进入注册表（运行——regedit）——找到HKEY_CURRENT_USER\Software\Microsoft\FTP\Accounts项，将其下面的子项（一般以FTP的IP命名）删除即可
* 来源:  [FTP服务器自动进入一个用户名，不能转换成其他用户名登录的解决方法](http://blog.sina.com.cn/s/blog_4b7041dd01010afl.html)
