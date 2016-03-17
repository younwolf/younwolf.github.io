---
layout: post  
title: 搭建Android开发环境04——Git  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Git  
description: 搭建Android开发环境04——Git  
---

　　版本控制(Revision control)是一种软体工程技巧，籍以在开发的过程中，确保由不同人所编辑的同一档案都得到更新。版本控制软件中我最常用的就是Git。  

　　Git是一个开源的分布式版本控制系统，用以有效、高速的处理从很小到非常大的项目版本管理。  

　　分布式相比于集中式的最大区别在于开发者可以提交到本地，每个开发者通过克隆（git clone），在本地机器上拷贝一个完整的Git仓库。  

　　大家都是是程序猿，所以版本控制的好处我就不说了，下面开始教程。　　

##  安装Git ##

　　先去[官网](http://www.git-scm.com/download/)下载。这下载速度有点慢，可能要翻墙。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/0.png" align="center"></p>
</center>

　　下载完安装，到这里按照实际情况勾选，我是全选。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/1.png" align="center"></p>
</center>

　　这是创建开始文件夹，按照实际情况。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/2.png" align="center"></p>
</center>

　　这是调整环境变量，默认即可。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/3.png" align="center"></p>
</center>

　　换行结束符，默认。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/4.png" align="center"></p>
</center>

　　终端风格，我喜欢默认的。第二个是Windows风格。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/5.png" align="center"></p>
</center>

　　启用文件缓存。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/6.png" align="center"></p>
</center>

##  安装TortoiseGit  ##

　　TortoiseGit是Windows下不错的一款Git客户端工具。  

　　先去官网下载[小乌龟](http://download.tortoisegit.org/)。如果你是墨守成规的人，那就点上面的稳定版下载。安装包下面有语言包。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/7.png" align="center"></p>
</center>

　　稳定版。

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/7-1.png" align="center"></p>
</center>

　　我选下面的预览版。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/7-2.png" align="center"></p>
</center>

　　先安装安装包，再安装语言包，一路默认即可。在开始菜单里面找到TortoiseGit文件夹，打开Settings，在这里更改语言。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/8.png" align="center"></p>
</center>

##  在Android Studio配置Git  ##

　　在Android Studio设置里打开Git，在里面设置Git的路径。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/9.png" align="center"></p>
</center>

　　然后点击Test，弹出Git版本则说明Git配置成功。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/10.png" align="center"></p>
</center>

##  在Android Studio使用Git  ##

　　菜单=>VCS。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/11.png" align="center"></p>
</center>

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Git/12.png" align="center"></p>
</center>

###  推荐阅读  ###

* [搭建Android开发环境01——Java](../09/Android-Develop-SetUp-Java.html)  
* [搭建Android开发环境02——Android SDK](../12/Android-Develop-SetUp-SDK.html)  
* [搭建Android开发环境03——Android Studio](../21/Android-Develop-SetUp-Studio.html)  
* [搭建Android开发环境03.1——Android Studio的优化](../24/Android-Develop-SetUp-StudioOptimize.html)  
* [搭建Android开发环境03.2——Hello World](../27/Android-Develop-SetUp-HelloWorld.html)  