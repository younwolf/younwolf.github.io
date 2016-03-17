---
layout: post  
title: 搭建Android开发环境03——Android Studio  
category: Android开发  
tags: Essay  
keywords: Android,搭建,环境,教程,Android Studio  
description: 搭建Android开发环境03——Android Studio  
---

　　到这里，Java环境搭建好了，Android SDK也下载好了，下面就开始神奇的Android Studio之旅。  

　　由于帝国已经不能愉快的访问Google了，我就把Android Studio（下文称**AS**）上传到网盘了：[Android Studio](http://yunpan.cn/cLUdkRLygJgZs "提取码：e6a0")，解压即可使用。  

##  第一次打开Android Studio  ##

　　打开AS目录=>`bin`=>`studio64.exe`（32位的打开studio.exe，下同）。第一次打开AS会提示导入设置，因为大部分人都是第一次接触，没有用过的设置，所以选第二个。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/0.png" align="center"></p>
</center>

　　等待一会进入欢迎界面，next之后进入安装类型，我们选`Custom`。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/1.png" align="center"></p>
</center>

　　来到设置主题界面，我们选择狂拽炫酷叼咋天的`Darcula`（我猜很少人会选择亮瞎眼的白色主题吧...）。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/2.png" align="center"></p>
</center>

　　在设置SDK目录界面，设置好我们自己下载并解压的SDK目录。不用理会红色警告。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/3.png" align="center"></p>
</center>

　　直到这里提示`Android SDK is up to date.`，Finish结束设置。

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/4.png" align="center"></p>
</center>

　　欢迎入坑。  

##  更新  ##

　　很多人都说AS很卡。的确，AS在前期是比较卡，但是后来AS更新升级之后优化了很多，不再是吃配置的小怪兽了。如果你的不是最新版，那么建议你升级吧。最新版是`AI-143.2461418`，由于AS一星期一更，所以这里发一下离线更新和在线更新的方法。  

####  离线更新  ####

　　检测是否为最新版：[https://dl.google.com/android/studio/patches/updates.xml](https://dl.google.com/android/studio/patches/updates.xml "Android Studio版本")  

　　图中红框即为现在的最新版本号。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/5.png" align="center"></p>
</center>

　　对比AS目录下的build.txt里面的版本号就知道是否要更新了。  

　　更新的补丁下载链接为：`https://dl.google.com/android/studio/patches/AI-`**当前安装版本号**`-`**更新的目标版本**`-patch-win.jar`。  

　　比如当前版本为`141.2279206`，最新版为`141.2288178`，则链接为`https://dl.google.com/android/studio/patches/AI-141.2279206-141.2288178-patch-win.jar`。  

　　接下来关闭所有与AS相关的进程，把下载的jar拷贝到AS目录外的任意位置，启动cmd，将路径定位到jar的文件夹中，输入`java -classpath `**jar名字**` com.intellij.updater.Runner install `**AS目录**，由于我用的是虚拟机，所以就直接放在桌面了，如图。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/6.png" align="center"></p>
</center>

　　按回车稍等一下就能更新完毕了。  

####  在线更新  ####

　　关闭所有与AS相关的进程，在AS目录中打开`bin`=>`studio64.exe.vmoptions`，最后一行加上：  

> -Didea.updates.url=https://dl.google.com/android/studio/patches/updates.xml  
> -Didea.patches.url=https://dl.google.com/android/studio/patches/  

　　启动AS，点击Check检查更新即可。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/7.png" align="center"></p>
</center>

　　由于我现在用的是最新版，所以显示这个。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/8.png" align="center"></p>
</center>

##  Android Studio优化  ##

　　关于更新之后还会卡，还有几招。  

* 改配置文件  
在AS目录中打开`bin`=>`studio64.exe.vmoptions`，修改前面的参数。改大点，但是量力而行，`Xmx`一般为你内存的四分之一即可，如果你的内存比较大可以大点。这是我的配置。  

<center>
    <p><img src="/../../../assets/images/Android/Develop/SetUp/Studio/9.png" align="center"></p>
</center>

* 关闭不需要的插件  
在设置里找到Plugins，关闭一些不常用或者没必要的插件也能提高运行速度。比如带有Google字样的，在帝国根本用不了，就可以关闭；还有用不到的版本控制也可以关闭。  
  
###  推荐阅读  ###

* [搭建Android开发环境01——Java](../09/Android-Develop-SetUp-Java.html)  
* [搭建Android开发环境02——Android SDK](../12/Android-Develop-SetUp-SDK.html)  