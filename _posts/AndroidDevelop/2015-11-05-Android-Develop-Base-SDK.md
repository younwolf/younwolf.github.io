---
layout: post  
title: Android开发基础01——Android SDK  
category: Android开发  
tags: Essay  
keywords: Android,基础,教程,Android SDK  
description: Android开发基础01——Android SDK  
---

　　想要开发Android，必不可少的就是Android SDK，因此了解SDK是必不可少的。这篇博客就是写有关Android SDK的。

## Android SDK结构

* **add-ons**  
这里面保存着附加库，比如 GoogleMaps，当然你如果安装了 OphoneSDK，这里也会有一些类库在里面。  
　　
* **build-tools**  
保存着一些 Android 平台相关通用工具，比如 adb、和 aapt、aidl、dx 等文件。  

  * **aapt**  
Android Asset Packaging Tool , 该工具可以查看, 创建, 更新ZIP格式的文档附件(zip, jar, apk)，也可将资源文件编译成二进制文件。  

  * **adb**  
android debug bridge 管理模拟器和真机的万能工具。  

  * **AIDL**  
Android Interface definition language，它是一种 Android 内部进程通信接口的描述语言，通过它我们可以定义进程间的通信接口。  

  * **Dexdump**  
Android Emulator 中可以找到一个名为 dexdump 的程序，通过 dexdump 可以查看出 apk 文件中的dex执行情况，粗略分析出原始java代码是什么样的，和Dot Net中的Reflector很像。  

  * **dx**  
Dx gongju 将.class字节码（bytecode）转换为Android字节码（保存在.dex文件中）。  
　　
* **docs**  
这里面是Android SDK API参考文档，所有的API都可以在这里查到。  
　　
* **extras**  
该文件夹下存放了google提供的USB驱动、Intel提供的硬件加速等附加工具包。  
　　
* **platforms**  
这是每个版本的SDK真正的文件，存放了不同版本的android系统。里面会根据APILevel划分SDK版本。  

  * **android.jar**  
是该版本的主要framework文件。  

  * **data**  
保存着一些系统资源。  

  * **skins**  
是Android模拟器的皮肤。  

  * **templates**  
工程创建的默认模板。  
　　
* **platform-tools**  
保存着一些Android平台相关通用工具，比如adb、和aapt、aidl、dx等文件，这里和platforms目录中tools文件夹有些重复，主要是从android2.3开始这些工具被划分为通用了。  

  * **adb**  
可以让你在模拟器或设备上安装应用程序的.apk文件，并从命令行访问模拟器或设备。你也可以用它把Android模拟器或设备上的应用程序代码和一个标准的调试器连接在一起。  

  * **Fastboot**  
刷机工具。  

  * **sqlite3**  
这个工具能够让你方便地访问SQLite数据文件。这些数据文件是由Android 应用程序创建并使用的。  
　　
* **samples**  
Android SDK自带的默认示例工程，对于SQLite数据库操作可以查看NotePad，对于游戏开发可以看Snake、LunarLander，对于Android主题开发Home则是android m5时代的主题设计原理。  
　　
* **sources**  
Android源代码。  
　　
* **system-images**  
Android虚拟机的镜像。
　　
* **tools**  
这里包含了android开发和调试的工具。draw9patch则是绘制android平台的可缩放png图片的工具，sqlite3可以在PC上操作SQLite数据库， 而monkeyrunner则是一个不错的压力测试应用，模拟用户随机按键，mksdcard则是模拟器SD映像的创建工具，emulator是Android SDK模拟器主程序，不过从android 1.5开始，需要输入合适的参数才能启动模拟器，traceview作为android平台上重要的调试工具。  

  * **ant**  
ant编译脚本。  

  * **ddms**  
这个工具集成了Dalvik（为Android平台定制的虚拟机（VM）），能够让你在模拟器或者设备上管理进程并协助调试。你可以使用它杀死进程，选择某个特定的进程来调试，产生跟踪数据，观察堆（heap）和线程信息，截取模拟器或设备的屏幕画面，还有更多的功能。
 
  * **draw9patch**  
Draw 9-patch工具允许你使用所见即所得（WYSIWYG）的编辑器轻松地创建NinePatch图形。它也可以预览经过拉伸的图像，高亮显示内容区域。
 
  * **emulator**  
Android SDK模拟器主程序，不过从android1.5开始，需要输入合适的参数才能启动模拟器。  
 
  * **Hierarchy Viewer**  
层级观察器工具允许你调试和优化你的用户界面。它用可视的方法把你视图（view）的布局层次展现出来，此外还给当前界面提供了一个具有像素栅格(grid)的放大镜观察器，这样你就可以正确地布局了。  
 
  * **monkeyrunner**  
一个不错的压力测试应用，模拟用户随机按键。  
 
  * **mksdcard**  
模拟器SD映像的创建工具。  
 
  * **templates**  
工程创建的默认模板。  
 
  * **traceview**  
这个工具可以将你的Android 应用程序产生的跟踪日志（trace log）转换为图形化的分析视图。  
　　

## Android SDK工具详解

　　Android SDK包含了各种各样的定制工具。  

* **Android Emulator(Android模拟器)**  
它是在你的计算机上运行的一个虚拟移动设备。你可以使用模拟器来在一个实际的Android运行环境下设计，调试和测试你的应用程序。  
　　
* **Adb**  
Android Debug Bridge(Android调试桥)工具可以让你在模拟器或设备上安装apk文件，并从命令行访问模拟器或设备。你也可以用它把Android模拟器或设备上的应用程序代码和一个标准的调试器连接在一起。  
　　
* **Hierarchy Viewer(层级观察器)**  
层级观察器工具允许你调试和优化你的用户界面。它用可视的方法把你的视图（view）的布局层次展现出来，此外还给当前界面提供了一个具有像素栅格(grid)的放大镜观察器，这样你就可以正确地布局了。  
　　
* **draw9patch**  
Draw 9-patch工具允许你使用所见即所得（WYSIWYG）的编辑器轻松地创建NinePatch图形。它也可以预览经过拉伸的图像，高亮显示内容区域。  
　　
* **Dalvik Debug Monitor Service(Dalvik 调试监视器服务)**  
这个工具集成了Dalvik（为Android平台定制的虚拟机（VM）），能够让你在模拟器或者设备上管理进程并协助调试。你可以使用它杀死进程，选择某个特定的进程来调试，产生跟踪数据，观察堆（heap）和线程信息，截取模拟器或设备的屏幕画面，还有更多的功能。  
　　
* **Android Asset Packaging Tool (aapt)**  
可以让你在模拟器或设备上安装应用程序的.apk文件，并从命令行访问模拟器或设备。你也可以用它把Android模拟器或设备上的应用程序代码和一个标准的调试器连接在一起。  
　　
* **sqlite3**  
这个工具能够让你方便地访问SQLite数据文件。这些数据文件是由Android 应用程序创建并使用的。  
　　
* **traceview**  
这个工具可以将你的Android 应用程序产生的跟踪日志（trace log）转换为图形化的分析视图。  
　　
* **mksdcard**  
帮助你创建磁盘映像（disk image），你可以在模拟器环境下使用磁盘映像来模拟外部存储卡（例如SD 卡）。  
　　
* **dx**  
Dx gongju 将.class字节码（bytecode）转换为Android字节码（保存在.dex文件中）。  
　　
* **UI/Application Exerciser Monkey**
Monkey是在模拟器上或设备上运行的一个小程序，它能够产生随机的用户事件流，例如点击(click)，触摸(touch)，手势（gestures），还有一系列的系统级事件。你可以使用Monkey来给你正在开发的程序做随机的、可重复的压力测试。  