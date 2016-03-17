---
layout: post  
title: 搭建Android开发环境03.1——Android Studio的优化  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Android Studio,优化  
description: 搭建Android开发环境03.1——Android Studio的优化  
---

　　这篇是承接上一篇[搭建Android开发环境03——Android Studio](https://18312847646.github.io/2015/10/21/Android-Develop-SetUp-Studio.html)的。主要讲讲怎样优化Android Studio以及使用技巧。  

##  关闭插件  ##

　　上篇末尾说到关闭一些不需要的插件，并没有具体说明是哪些，这篇就在这里向大家一一说明。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/Optimize/0.png" align="center"></p>
</center>

* Android NDK Support：原生应用开发。初学者基本很难接触到，以后需要时再打开。  

* CVS Integration：一种版本控制系统，一般用Git，所以禁用。  

* Google *：Google的各种东西，由于在天朝帝国基本用不上，所以禁用。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/Optimize/1.png" align="center"></p>
</center>

* hg4idea：一种版本控制系统，禁用。  

* SDK Updater：SDK更新，一般用SDK里面的，所以禁用。  

* Subversion Integration：一种版本控制系统，禁用。  

##  文件编码  ##

　　在天朝的电脑上，文件编码都是默认的使用GBK，由于兼容性问题，建议全部都统一使用UTF-8。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/Optimize/2.png" align="center"></p>
</center>

##  显示行号  ##

　　为什么显示行号我就不解释了。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/Optimize/3.png" align="center"></p>
</center>

##  检查更新  ##

　　对于检查更新，上篇漏了说，就是设置里的检查类型。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/Optimize/4.png" align="center"></p>
</center>

* Stable Channel：正式版，只会获取最新的正式版本。  

* Beta Channel：测试版，只会获取最新的测试版本。  

* Dev Channel：开发版，只会获取最新的开发版本。  

* Canary Channel：预览版，只会获取最新的预览版本。  

　　还有一些，以后补上。  

###  推荐阅读  ###

* [搭建Android开发环境01——Java](../09/Android-Develop-SetUp-Java.html)  
* [搭建Android开发环境02——Android SDK](../12/Android-Develop-SetUp-SDK.html)  
* [搭建Android开发环境03——Android Studio](../21/Android-Develop-SetUp-Studio.html)  