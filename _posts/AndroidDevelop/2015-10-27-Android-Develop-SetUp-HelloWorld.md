---
layout: post  
title: 搭建Android开发环境03.2——Hello World  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Android Studio,HelloWorld  
description: 搭建Android开发环境03.2——Hello World  
---

##  万年Hello World  ##

　　Hello World，任何语言的第一个程序。  

　　打开Android Studio，新建一个项目。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/0.png" align="center"></p>
</center>

　　输入程序名称。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/1.png" align="center"></p>
</center>

* Application name: 应用程序名。  

* Company Domain: 公司域名。  

* Package name: Android程序的包名，系统会将这个包名作为程序唯一的标识。  

　　选择程序兼容的最低版本，Android 4.0.3足以，然后一路默认next到Finish。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/2.png" align="center"></p>
</center>

　　等一下就创建好工程了。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/3.png" align="center"></p>
</center>

　　连接手机（建议）或者用虚拟机。由于刚买新手机还没有Root，这里就用虚拟机了。点击菜单=>`Run`=>`Run 'app'`，弹出一个框，点击OK即可安装。要想一直都默认这个设置，勾上选框即可，不勾选每次运行都会弹出这个框。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/4.png" align="center"></p>
</center>

　　在虚拟机上安装完成。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/5.png" align="center"></p>
</center>

##  又见Hello World  ##

　　这里借助Hello World说说在Android Studio里项目的结构。  

　　新建的工程，默认是Android视图。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/6.png" align="center"></p>
</center>

　　第一个是app模块。一个模块包含：  

* manifests  
  * AndroidManifest.xml  
Android应用的配置文件，所有工程都必须有这个文件。这个文件列出了应用程序所提供的所有组件，比如：窗口、服务等。  

* java  
这里是程序的Java源代码，和Java的结构相似。这里有两部分。  
  * 无`androidTest`： Java源代码。  
  * 有`androidTest`： 测试类。  

* res  
资源目录，该目录存储了指定类型的资源。  
  * drawable： 图像资源。  
  * layout： 布局资源。  
  * menu： 菜单资源。  
  * mipmap： 图像资源（与drawable相比，mipmap会在缩放上提供一定的性能优化）。  
  * values： 可以被编译成很多种类型的XML资源。  

　　接下来就是Gradle Scripts了。  

* build.gradle: 工程配置。  
* build.gradle： 模块配置。  
* proguard-rules.pro： 混淆配置文件。  
* gradle.properties： gradle配置文件。  
* settings.gradle： 工程模块配置。  
* local.properties： 本地配置。  

##  Project Structure  ##

　　工程配置。打开菜单=>`File`=>`Project Structure`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/7.png" align="center"></p>
</center>

* Properties  
  * Compile Sdk Version： 编译的版本，使用最新。  
  * Build Tool Version： 构建工具的版本，使用最新。  
  * Incremental Dex： dex增量编译，实验性功能，据说可以加快编译速度。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/HelloWorld/8.png" align="center"></p>
</center>

* Flavors  
  * Min Sdk Version： 最小兼容版本，4.0.3即可。  
  * Application Id： 设备和Google Play用来标识应用的Id。  
  * Target Sdk Version： 目标版本，最高即可。  
  * Version Code： 程序版本，用于商店判断新旧。  
  * Version Name： 版本号，用于用户判断新旧。  

###  推荐阅读  ###

* [搭建Android开发环境01——Java](../09/Android-Develop-SetUp-Java.html)  
* [搭建Android开发环境02——Android SDK](../12/Android-Develop-SetUp-SDK.html)  
* [搭建Android开发环境03——Android Studio](../21/Android-Develop-SetUp-Studio.html)  
* [搭建Android开发环境03.1——Android Studio的优化](../24/Android-Develop-SetUp-StudioOptimize.html)  