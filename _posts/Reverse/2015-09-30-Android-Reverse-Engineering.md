---
layout: post  
title: 反编译之——手机端反编译教程  
category: 反编译  
tags: Android,反编译,手机端  
description: 反编译之——手机端反编译教程  
---

　　今天我就写一个反编译教程，预计有两篇，这篇是手机端反编译的，下一篇是PC端的。废话不多说，下面进入正题。  

###  前提  ###

1. 手机需root  
2. [apktool](http://pan.baidu.com/s/1t3n2I "密码: 7yse")  
3. 据说还要有[BusyBox](http://pan.baidu.com/s/1nt7tW6l "密码: j3pf")  

##  教程  ##

1. 安装apktool  
　　一般来说，网上的都是压缩包，需要配置比较多东西（共享的是直装包）。对两种apktool分别写教程。  
   - 压缩包:  
　　解压apktool，放sdcard根目录（/sdcard/），不建议改名，直接apktool。进apktool文件夹，有一个也是唯一一个apk，安装它。打开，进入sdcard，找到apktool文件夹，长按，点击`设为apktool数据目录`之类的按钮，视apktool版本而定。  
   - 直装包   
　　安装apk，打开之后会自动弹出一个更新，点更新即可。一般这种安装方式是不用像上面的方法那样设置默认目录的，如果你的apktool不正常，请像上面那样操作一遍。  

2. 安装framework（这一步是针对反编译系统应用的，如果只是反编译普通应用，则可跳过）  
　　返回根目录，进入system，再进入framework，找到framework-res.apk，点击apk，点击`作为framework导入`。  

3. 反编译  
　　把需要反编译的apk找出来，作者是单独放在了一个文件夹里。这里需要提醒的是，路径和apk名字都不能有中文。点击apk，可选的有`反编译全部`、`反编译dex`、`反编译资源`。反编译全部就是把整个apk都反编译，反编译dex就是只反编译dex部分，反编译资源就是反编译res和resources.arsc。不过一般作者是直接反编译全部，如果不确定需要改什么，也可以直接反编译全部。点击反编译按钮之后，剩下的就是等待反编译过程结束，等待时间视apk大小而定。  

4. 完  