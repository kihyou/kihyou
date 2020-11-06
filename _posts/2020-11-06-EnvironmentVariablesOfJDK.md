---
layout: post
title:  "java:jdk环境变量配置"
date:   2020-11-06
category: java
---
## 配置单个JDK  
1. 右击“此电脑”->属性  
2. 高级系统设置  
  ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022103921994-840566324.png)  
3. 高级->环境变量  
  ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022104048126-2097596368.png)  
4. 配置环境变量（推荐：系统变量）  
    1. 新建JAVA_HOME  
      ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022104112034-1718989990.png)  
    2. 新建/修改CLASSPATH  
      `.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`  
      ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022104429418-1416311406.png)  
    3. 修改PATH变量  
      `%JAVA_HOME%\bin`  
      `%JAVA_HOME%\jre\bin`  
      ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022104225633-2125731679.png)  
5. cmd运行java、javac检测是否安装成功  
  ![](https://img2020.cnblogs.com/blog/1752736/202010/1752736-20201022104211838-881716923.png)  

## 关于配置多个JDK  
  * 推荐：[JDK环境变量配置，实现多个版本的JDK环境变量任意切换配置(Windows7 / Windows10 )](https://www.cnblogs.com/yuyu666/p/12666506.html)  
