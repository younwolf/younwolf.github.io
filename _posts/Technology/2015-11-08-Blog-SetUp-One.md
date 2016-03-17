---
layout: post  
title: 个人博客搭建1——Windows  
category: 技术  
tags: Essay  
keywords: 博客,教程  
description: 个人博客搭建1——Windows  
---

　　博客（英语：Blog，为Web Log的混成词），指 log on the web，即在网络上纪录，是一种由个人管理、张贴新的文章、图片或影片的网站或在线日记，用来纪录、抒发情感或分享信息。博客上的文章通常根据张贴时间（Chronological Order），以倒序方式由新到旧排列。——来自 自由的百科全书  

　　阮一峰老师说过：喜欢写 Blog 的人，会经历三个阶段：  

> 第一阶段，刚接触 Blog，觉得很新鲜，试着选择一个免费空间来写。  
> 第二阶段，发现免费空间限制太多，就自己购买域名和空间，搭建独立博客。  
> 第三阶段，觉得独立博客的管理太麻烦，最好在保留控制权的前提下，让别人来管，自己只负责写文章。  

　　今天就来写写在github上的个人博客的搭建。  

　　github 是一个利用 Git 进行版本控制、专门用于存放软件代码与内容的共享虚拟主机服务。  

　　在 [github](https://github.com/) 上搭建 blog 。既拥有绝对管理权，又享受 github 带来的便利——不管何时何地，只要向主机提交 commit，就能发布新文章。更妙的是，这一切还是免费的，github 提供无限流量。  

　　但是对于一个新手来说，看到一大堆源码，只会让人头晕脑涨，不知何处入手。他希望看到的是，一个简明易懂的网页，说明每一步应该怎么做。因此，github 就设计了 Pages 功能，允许用户自定义项目首页，用来替代默认的源码列表。所以，github Pages 可以被认为是用户编写的、托管在 github 上的静态网页。  

　　github 提供模板，允许站内生成网页，但也允许用户自己编写网页，然后上传。有意思的是，这种上传并不是单纯的上传，而是会经过 Jekyll 程序的再处理。  

### So what is Jekyll, exactly? ###

> Jekyll is a simple, blog-aware, static site generator.  

　　根据官方说法，`Jekyll` 是一个简单的静态博客站点生成器。  

　　我们需要做的就是在本地写好博客，然后上传到服务器上。优点很明显：  

1. 免费、无限流量。  
2. Revision control，你懂的。  
3. 单纯写文章即可，无需管理。  

　　安装 jekyll 之前需要有一些环境：  

* Ruby  
* RubyGems  
* NodeJS

　　安装好这些之后，


### 安装 Ruby ###

　　Ruby 在不同平台有不同的安装方式，本教程针对Windows用Ruby的安装器来安装。  

　　前往[官网](http://rubyinstaller.org/downloads/)根据自己系统位数下载最新版。  

<center>
    <p><img src="/../../../assets/images/Technology/Blog/0.png" align="center"></p>
</center>

　　下载完安装，默认英文。同意协议之后来到这里，勾选 **`Add Ruby executables to your PATH`**，安装器会自动添加环境变量。不建议修改安装路径，如果更改了路径，路径中间不要出现中文以及空格。  

<center>
    <p><img src="/../../../assets/images/Technology/Blog/1.png" align="center"></p>
</center>

　　安装完成后打开命令行，输入：  

    ruby -v  

　　如果输出当前安装的版本，即表示Ruby安装成功。  

### 安装 DevKit ###

　　DevKit 是一个在 Windows 上帮助简化安装及使用 Ruby C/C++ 扩展如 RDiscount 和 RedCloth 的工具箱。  

　　还是前往[官网](http://rubyinstaller.org/downloads/)根据自己系统位数下载最新版。  

<center>
    <p><img src="/../../../assets/images/Technology/Blog/2.png" align="center"></p>
</center>

　　下载完双击，解压到非中文无空格的路径中。  

<center>
    <p><img src="/../../../assets/images/Technology/Blog/3.png" align="center"></p>
</center>

　　新建命令行窗口，cd 到路径中，依次输入：  

	ruby dk.rb init  
	notepad config.yml  

　　在打开的记事本中，末尾的斜杠改成相反的（如 `/` 改成 `\`），保存文件并退出。  

### 安装 Jekyll ###

　　经过上面安装，gem 已经正确安装。新建命令行窗口，输入：  

	gem -v  

　　如果能够输出 gem 的版本，即说明 gem 确实安装成功了。  

　　新建命令行窗口，输入：  

	gem install jekyll  

> All of Jekyll’s gem dependencies are automatically installed by the above command, so you won’t have to worry about them at all.  

　　根据官方文档，所有的 Jekyll 的 gem 依赖包都会被自动安装。等待一下即可完成安装（在天朝会比较慢）。如果中途弹出网络权限，允许即可。安装完成可新建命令行窗口输入以下命令来验证是否安装成功：  

	jekyll -v  

　　如果输出 jekyll 的版本，即说明安装成功。  

### 使用jekyll ###

　　Now that you’ve got everything installed, let’s get to work!  

　　现在新建命令行窗口，cd 到要新建博客的路径，输入如下命令：  

	jekyll new myblog  

　　名为 myblog 的博客即可自动生成。继续输入：  

	cd myblog
	jekyll serve

　　现在在浏览器中输入 `http://localhost:4000` 即可浏览新建的博客。  

　　在 myblog 文件夹中的 _posts 文件夹中依据现有的博客格式添加用 markdown 写的文章即可完成添加博客。  

　　至此 Windows 端的博客搭建已完成了。  