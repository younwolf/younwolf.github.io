---
layout: post  
title: 搭建Android开发环境05——Genymotion  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Genymotion  
description: 搭建Android开发环境05——Genymotion  
---

　　Genymotion是一套完整的工具，它提供了Android虚拟环境。它简直就是开发者、测试人员、推销者甚至是游戏玩家的福音。  

##  安装VirtualBox  ##
　　由于Genymotion是基于VirtualBox的，所以我们先安装[VirtualBox](https://www.virtualbox.org/)。进入官网点击大大的`download`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/0.png" align="center"></p>
</center>

　　点击`x86/amd64`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/1.png" align="center"></p>
</center>

　　安装VirtualBox基本上一路默认，然后安装虚拟网卡，这里点击安装。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/2.png" align="center"></p>
</center>

##  安装Genymotion  ##

　　安装完VirtualBox就开始安装Genymotion了。进入[官网](https://www.genymotion.com/#!/)。找到`Get started with Genymotion`，点击`download`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/3.png" align="center"></p>
</center>

　　选不带VirtualBox的版本下载。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/4.png" align="center"></p>
</center>

　　有账号的登陆，没账号的注册。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/5.png" align="center"></p>
</center>

　　安装完打开，打开设置。Account登陆刚才注册的账号。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/6.png" align="center"></p>
</center>

　　ADB选择自己的SDK目录。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/7.png" align="center"></p>
</center>

##  在Android Studio设置Genymotion  ##

　　在设置里打开Plugins。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/8.png" align="center"></p>
</center>

　　搜索Genymotion，安装完重启Android Studio。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/9.png" align="center"></p>
</center>

　　打开设置，在Genymotion里面设置路径即可。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/10.png" align="center"></p>
</center>

##  在Android Studio使用Genymotion  ##

　　在工具栏点击手机图标。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/11.png" align="center"></p>
</center>

　　点击new即可新建虚拟机。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Genymotion/12.png" align="center"></p>
</center>

###  推荐阅读  ###

* [搭建Android开发环境01——Java](../../10/09/Android-Develop-SetUp-Java.html)  
* [搭建Android开发环境02——Android SDK](../../10/12/Android-Develop-SetUp-SDK.html)  
* [搭建Android开发环境03——Android Studio](../../10/21/Android-Develop-SetUp-Studio.html)  
* [搭建Android开发环境03.1——Android Studio的优化](../../10/24/Android-Develop-SetUp-StudioOptimize.html)  
* [搭建Android开发环境03.2——Hello World](../../10/27/Android-Develop-SetUp-HelloWorld.html)  
* [搭建Android开发环境04——Git](../../10/30/Android-Develop-SetUp-Git.html)  