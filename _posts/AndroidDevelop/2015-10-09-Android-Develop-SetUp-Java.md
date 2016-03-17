---
layout: post  
title: 搭建Android开发环境01——Java  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Java  
description: 搭建Android开发环境01——Java  
---

　　正所谓“工欲善其事必先利其器”，要开发Android，必须先把环境搭建好。这个系列便是写怎样搭建Android开发环境的。  

　　Android所有的应用程序都是使用Java编写的（底层是用C/C++），所以开发Android首先就是搭建Java环境了。  

　　想要搭建Java环境，当然需要先安装JDK。“巧妇难为无米之炊”，现在就去[官网](http://www.oracle.com/technetwork/java/javase/downloads/index.html)下载JDK吧。  

　　打开[官网](http://www.oracle.com/technetwork/java/javase/downloads/index.html)，点击`download`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/1.png" align="center"></p>
</center>

　　跳转到下载界面，点击`Accept License Agreement`（接受许可协议），然后点击`jdk-8u60-windows-x64.exe`下载64位的JDK（如果你的系统是32位的，那只能选择上面那个x86的）。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/2.png" align="center"></p>
</center>

　　下载完了以后直接安装，点下一步。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/3.png" align="center"></p>
</center>

　　这里可以更改JDK的安装目录（**不要有中文路径，这是常识，只说一遍**）。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/4.png" align="center"></p>
</center>

　　这里可以更改JRE的安装目录。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/5.png" align="center"></p>
</center>

　　可能很多人都不知道JDK和JRE的区别。  

* JDK（Java Development Kit）是Java语言的软件开发工具包（SDK），没有JDK的话，无法编译Java程序。  
* JRE（Java Runtime Environment，Java运行环境），运行Java程序所必须的环境集合，包含JVM标准实现及Java核心类库。  

　　这样就算安装完成了，点击关闭即可。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Java/6.png" align="center"></p>
</center>

　　别高兴得太早，这只是安装了Java环境，真正的环境还没有配置好。下面就来配置环境。  

　　打开环境变量（不同系统有微小差异，这里以win8.1为例）。右键`这台电脑`=>`属性`=>`高级系统设置`=>`环境变量`。在系统变量：  

* 新建`JAVA_HOME`  
JDK的安装路径  
* 修改`PATH`  
最前面添加`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`  
* 创建`CLASSPATH`  
`.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`  

　　配置好环境需要检测一下，win+R=>`CMD`=>`Javac`，如果出来一大堆，则说明Java环境搭建成功了。  