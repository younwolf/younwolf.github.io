---
layout: post  
title: 反编译之——PC端反编译教程  
category: 反编译  
tags: 反编译  
description: 反编译之——PC端反编译教程  
---

　　大家好，今天我要带给大家的是反编译篇的第二篇——PC端反编译。下面开始我们的PC端反编译教程。 

###  前提  ###

1. Java环境。  
2. apktool PC版，这个类型就比较多了，下面会一一解释。   

##  教程  ##

* apktool CMD版   
　　一般网上下载的都是压缩包，解压缩就可以使用了。把apk文件放在文件夹里面（还是一样路径和apk都不能有中文，一般CMD版会要求apk名是123.apk），点击cmd后缀的脚本文件就可以进行反编译了（也可以直接把apk文件拖到cmd文件上）  

<center>
    <p><img src="/../../../assets/images/PC/Reverse/Engineering/apktool-CMD.png" align="center"></p>
</center>

　　按照界面说明 就可以反编译了。  

* ApkIDE（改之理）  
　　这个操作比较简单，功能也比较多比较强大。打开ApkIDE.exe，菜单点击项目-打开apk，选择apk即可（打开ApkIDE.exe之后直接拖拽apk到界面也是可以的），稍等片刻反编译便完成了。我以后写的破解软件实战大部分都会使用这款工具进行反编译。  

<center>
    <p><img src="/../../../assets/images/PC/Reverse/Engineering/apktool-apkIDE.png" align="center"></p>
</center>

　　反编译之后可以用ApkIDE直接修改，修改完之后记得保存，然后菜单点击编译-编译apk即可回编译（回编译成功与否取决于软件是否有校验保护以及你修改的代码是否正确）。  

* 其他一些反编译工具  
　　这里介绍了我比较常使用的两个反编译工具，实际上反编译工具有很多，比如Java反编译工具jd-ui（直接查看java代码）、dex2jar（把Dalvik虚拟机的dex文件转换回标准Java的class文件的工具）、Android逆向助手（这个没用过，表示我听到这是一个傻瓜式反编译工具就不想用了，技术党对于技术含量不高的东西不感兴趣）、baksmali（把classes.dex转成.smali的）、AXMLPrinter2（专门转换XML文件的）、Jodeclipse（Jode的Eclipse插件）、JadClipse（Jad的Eclipse插件）。  

　　由于有很多工具我很少用，所以就不一一赘述了。这么多反编译工具，相信反编译是没问题了，对于我没说明使用方法的工具，可以Google。  

###  结语  ###

　　最后，我送大家一句话，Google是最好的老师（Google的搜索比度娘好太多专业太多，不过鉴于不是每个人都会翻墙，如果你不会翻墙，请别说认识我）。  