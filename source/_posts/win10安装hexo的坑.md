---
title: win10安装hexo的坑
tags: [hexo]
date: 2020-07-20 00:14:06
permalink:
categories: 个人博客
description:
image:
---
<p class="description">使用github+hexo搭建个人博客，之前使用另一台笔记本上搭建的，现在换了笔记本，所以要新搭建本地环境，就是安装和配置hexo。本来以为是很简单的事情，结果就碰到了坑，折腾了几个小时。。。</p>

<img src="hexo.jpg" alt="" style="width:100%" />

<!-- more -->

#### 背景
使用github+hexo搭建个人博客，之前使用另一台笔记本上搭建的，现在换了笔记本，所以要新搭建本地环境，就是安装和配置hexo。本来以为是很简单的事情，结果就碰到了坑，折腾了几个小时。。。  

hexo：轻量级的博客系统，本身不需要部署到服务器，会把markdown文件生成静态的html文件  

githubPage：github的githubPage可以托管静态页面

本地计算机系统：Win10 64位

#### 问题
具体问题为：  
使用npm全局安装hexo之后，竟然在powershell和CMD中无法识别hexo命令。  
安装hexo的命令：

```shell
npm install -g hexo
```
powershell中执行hexo -v 命令报错
![win10安装hexo的坑-2020-07-19-18-43-40](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/win10安装hexo的坑-2020-07-19-18-43-40.png)

我是全局安装的，应该是安装完之后在任意路径之下都可以调用hexo命令的。  
我就到hexo的包路径之下执行hexo命令试一下，竟然也不能识别，这我就搞不懂为什么了，于是百度之。没找到具体的原因，但是找到了两种解决方案。  

#### 方案一
安装 hexo-cli包，然后再gitbash命令行工具下执行hexo命令。  
安装hexo-cli工具：
```
npm install -g hexo-cli
```
因为我已经安装过hexo-cli了，所以再次安装给我报错了。

![win10安装hexo的坑-2020-07-19-19-34-54](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/win10安装hexo的坑-2020-07-19-19-34-54.png)

安装完之后，在gitbash命令行工具中执行hexo命令，可以看到是成功的：

![win10安装hexo的坑-2020-07-19-19-37-08](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/win10安装hexo的坑-2020-07-19-19-37-08.png)

#### 方案二
把hexo包的安装路径下，包含hexo.cmd文件的路径添加到环境变量之中。 

我本地的路径为：D:\Tool\nodeJs\node_global\node_modules\hexo\node_modules\.bin  

将上面的路径添加到环境变量path中之后，再在桌面打开powershell，并执行hexo命令，就发现可以执行成功了：

![win10安装hexo的坑-2020-07-19-19-32-32](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/win10安装hexo的坑-2020-07-19-19-32-32.png)


最终我选择了第二种方案，第一种方案，只能再gitbash中执行还是有些限制的，有时候会不方便。


#### 插曲
在查找问题的过程中，注意到安装hexo的时候，有两个warning警告信息：

![win10安装hexo的坑-2020-07-19-19-44-51](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/win10安装hexo的坑-2020-07-19-19-44-51.png)

就怀疑是不是这个的问题，导致hexo的命令不能识别。于是也百度了一下这个警告的相关信息。网上的说法是，这个警告是因为在苹果的机器上需要安装fsevents这个模块，使用的windows和Linux的系统，可以忽略这个警告。

<hr />