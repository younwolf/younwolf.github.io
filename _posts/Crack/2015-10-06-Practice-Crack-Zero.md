---
layout: post  
title: 软件破解第一战  
category: 破解  
tags: Android,破解,实战  
description: 软件破解第一战  
---

　　首先，这是一个翻墙软件，至于为什么翻墙以及翻墙之后能干什么，找度娘。这个软件申请账号后，有一个时间限制（以前有一个活动可以得到试用期，不过现在活动已经过了，即使新申请的账号也不能试用了，只能购买VIP）。本文的目的就是去除这个限制。  

　　软件：[thorvpn](http://pan.baidu.com/s/1qW24wpQ "密码: rwvt")  
  
##  教程  ##

　　反编译软件（不会反编译的看这里：[PC端](../03/PC-Reverse-Engineering.html "反编译之——PC端反编译教程")、[手机端](../../09/30/Android-Reverse-Engineering.html "反编译之——手机端反编译教程")），搜索图中文字“`您的服务已到期`”。很幸运，可以搜索出来，文件位置在如图第一个框，第77行。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/1.png" align="center"></p>
</center>

　　继续搜索`name`后面的`dlg_message_service_expired`。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/2.png" align="center"></p>
</center>

　　搜索`dlg_message_service_expired`之后出来四个结果，如图。我们应该找的是第一个。因为第一个有一个ID。至于为什么不是其他三个，这涉及到Android编程知识，这里就不叙述了。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/3.png" align="center"></p>
</center>

　　继续搜索ID后面的字符串`0x7f090057`。  

　　搜索ID之后出来两个结果，第一个是原来的，不用管。第二个就是我们要找的。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/4.png" align="center"></p>
</center>

　　找到ID的位置。我们的重点来了，在ID上面，红框圈住的地方。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/5.png" align="center"></p>
</center>
  
####  这个是Dalvik指令集三种跳转之一的if跳转，解释见下：   ####

#####  if跳转又分两种：  #####

　　第一种指令为`if-test vA,vB,+CCCC`  

> 比较vA寄存器和vB寄存器的值，如果比较结果满足就跳转到CCCC指定的偏移处。  
> `if-test`类型的指令有以下几条：  
> `if-eq vA, vB, CCCC` 如果vA == vB，跳转到CCCC  
> `if-ne vA,vB, CCCC` 如果vA != vB，跳转到CCCC  
> `if-lt vA,vB, CCCC` 如果vA < vB，跳转到CCCC  
> `if-ge vA, vB, CCCC` 如果vA >= vB，跳转到CCCC  
> `if-gt vA,vB, CCCC` 如果vA > vB，跳转到CCCC  
> `if-le vA,vB, CCCC` 如果vA <= vB，跳转到CCCC  

　　第二种指令为`if-testz vAA,+BBBB`  

> 用vAA寄存器和0比较，，如果比较结果满足或值为0时就跳转到BBBB指定的偏移处。  
> `if-testz`类型的指令有以下几条：  
> `if-eqz vAA, BBBB` 如果vAA == 0，跳转到BBBB  
> `if-nez vAA, BBBB` 如果vAA != 0，跳转到BBBB  
> `if-ltz vAA, BBBB` 如果vAA < 0，跳转到BBBB  
> `if-gez vAA, BBBB` 如果vAA >= 0，跳转到BBBB  
> `if-gtz vAA, BBBB` 如果vAA > 0，跳转到BBBB  
> `if-lez vAA, BBBB` 如果vAA <= 0，跳转到BBBB  

**==是等于、!=是不等于、<是小于、>是大于、<=是小于等于、>=是大于等于。**

　　在上图的红框里，程序判断v0和v3的值，很明显判断过程是v0>=v3，结果不满足，则程序继续向下执行。  

　　执行到ID部分，显示字符串，就是显示“您的服务已到期”。  

　　那么如果在显示字符串之前，在判断时间是否到期的时候，跳转到另一个分支，不就可以达到破解的目的了吗？  

　　既然判断指令是`if-ge`，我们就改成与之相反的`if-lt`。改完保存，回编译，签名安装试试。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/6.jpg" align="center"></p>
</center>

　　点击按钮虽然没弹出服务已到期，不过也没成功连接，说明破解失败了。  

　　既然失败了，说明这个跳转不是判断时间是否超时的，我们继续向上寻找。我们可以看到，在`if-ge`之上，已经没有if跳转了：  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/7.png" align="center"></p>
</center>

　　虽然已经没有if跳转了，不过我们继续向上可以看到`.method`。`.method`是反汇编代码声明方法的指令。  

　　现在怎么办呢？搜索`.method`那行括号里面的：  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/8.png" align="center"></p>
</center>

　　搜索出来三个结果，我们选第三个。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/9.png" align="center"></p>
</center>

　　为什么呢，因为第三个是跳转到这里的，就是说第三个是这个的上级。  

　　按照思路，找到这里。离跳转最近的地方有一个if跳转。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/10.png" align="center"></p>
</center>

　　`if-eqz v0, :cond_0`，意思是如果v0==0，跳转到`cond_0`。  

　　很明显这里没有跳转，因为没有跳转才能继续执行下面的指令。  

　　我们把它改成`if-nez`，保存，回编译，签名安装。  

　　结果还是一样，点击按钮没反应。我们继续破解。  

　　在这个if跳转之上，有一个`:cond_2`。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/11.png" align="center"></p>
</center>

　　就是说，这是跳转之后来到`cond_2`的。  

　　我们找到`cond_2`的源头。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/12.png" align="center"></p>
</center> 

　　就在上面不远处，老规矩，修改`if-nez`为`if-eqz`。  

　　保存，回编译，签名安装。  

　　点击按钮.弹出这个.恭喜你.破解成功了。  

<center>
    <p><img src="/../../../assets/images/Practice/Crack/Zero/13.jpg" align="center"></p>
</center> 

　　教程到这里结束了。  

####  请尊重他人劳动成果，转载请注明来自[77.](http://18312847646.github.io "贔!忍!震!狡!")的博客：[18312847646.github.io](http://18312847646.github.io "贔!忍!震!狡!")  ####