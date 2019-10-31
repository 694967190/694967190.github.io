---
layout: post
title: Python记录
date: 2019/10/31
categories: blog
tags: [Python,编程]
description: 串口连接传递的不只是数据。
---

<p>10月31日,尝试使用python连接串口</p>
<p>调用了python的serial库,安装方法pip install pyserial </p>
<p>具体记录主要函数</p>
<p>变量名=serial.Serial(“端口”,波特率,timeout=0.5)//通过COM连接串口</p>
<p>ser.open() //打开端口 ser.close()#关闭端口</p>
<p>data = ser.read(20)读取xxx个字符</p>
<p>ser.isOpen()//检查串口是否开启</p>
<p>read(size=1)：//从串口读size个字节</p>
<p>write(xx)//发送字节</p>
<p></p>
<p>链接记录:将字符串转为字典！:https://www.cnblogs.com/OnlyDreams/p/7850920.html</p>
<p>常用正则表达式记录</p>
<p> print(re.sub("<[^>]*>", "", str(xx)))  //可以取消掉标签</p>
<p>2019/10/31 上海记</p>













