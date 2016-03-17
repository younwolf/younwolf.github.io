---
layout: post  
title: 搭建Android开发环境02——Android SDK  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,SDK  
description: 搭建Android开发环境02——Android SDK  
---

　　SDK：（Software Development Kit）软件开发工具包。被软件开发工程师用于为特定的软件包、软件框架、硬件平台、操作系统等建立应用软件的开发工具的集合。  

　　因此，Android SDK 指的是Android专属的软件开发工具包。  

　　搭建好Java环境之后，便可以下载Android SDK了。Android SDK是不用安装的，解压出来即可使用。由于帝国把Google封了，我们没法直接下载，我把我平时用的Android SDK精简然后上传到网盘了：[Android SDK](https://yunpan.cn/crbrQdgsVdNhY "密码:4993")。全部下载下来直接解压即可，有更新的时候请看按照更新日期命名的文件夹，日期文件夹直接解压覆盖即可。  

　　Android SDK这样就弄好了。如果你是万年不更新的，那你可以不用看下去了，如果你追求最新版新技术，那就继续看下去吧。  

　　由于我们伟大的帝国把Google封了，我们无法直接下载，也无法更新Android SDK了。但是追求自由的力量是无限的，网上有很多热心人给我们各种各样的方法，我最常用的就是反代理了。  

　　打开`C:\Windows\System32\drivers\etc\hosts`，在里面添加一行：`133.130.63.27 dl-ssl.google.com`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/SDK/1.png" align="center"></p>
</center>

　　在Android SDK目录里打开*SDK Manager.exe*，然后打开设置。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/SDK/2.png" align="center"></p>
</center>

　　如图设置。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/SDK/3.png" align="center"></p>
</center>

　　重启*SDK Manager.exe*，以后就可以在线更新Android SDK了。  

----------

　　为了以后方便使用Android SDK，这里顺带把有关SDK的所有设置都一起设置完。  

　　打开环境变量：  

* 新建`ANDROID_SDK`  
Android SDK的目录。  
* 修改`PATH`  
最前面添加`%ANDROID_SDK%\tools;%ANDROID_SDK%\platform-tools;`  

　　设置过上面的之后，win+R=>`CMD`=>`adb`，如果出来一大堆，则说明设置成功了。  

###  推荐阅读  ###

* [搭建Android开发环境01——Java](../09/Android-Develop-SetUp-Java.html)  