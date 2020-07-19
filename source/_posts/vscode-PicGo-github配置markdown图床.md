---
title: vscode+PicGo+github配置markdown图床
tags: [vscode]
date: 2020-07-19 22:36:45
permalink:
categories: vscode
description: vscode
image:
---
<p class="description">
<span>markdown，语法简洁、排版美观，是个好东西。</span></br>
<span>PicGo，使用简便、支持多平台图床，是个好东西。</span></br>
<span>vscode，支持Markdown语法，又有PicGo插件，真香！</span>
</p>

<img src="markdown.jpg" alt="" style="width:100%" />

<!-- more -->

#### vscode下载PicGo插件
1. 在vscode的marketplace中搜索插件“PicGo”
![20200718000841](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/20200718000841.png)

2. 点击install按钮安装插件

#### 配置github
1. 创建一个新仓库
![vscode+PicGo+github配置markdown图床-2020-07-18-01-07-38](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-07-38.png)
创建的仓库类型要是public。(注意：因为是公开的仓库，上传的图片注意个人隐私)
![vscode+PicGo+github配置markdown图床-2020-07-18-01-12-40](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-12-40.png)

2. 在github的设置中生成token  
在settings - developer settings - Personal access tokens中点击“Generate new token”按钮，生成新的token。  
这个token需要立即复制下来，过后不会再显示。
![vscode+PicGo+github配置markdown图床-2020-07-18-01-15-31](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-15-31.png)
![vscode+PicGo+github配置markdown图床-2020-07-18-01-17-38](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-17-38.png)
![vscode+PicGo+github配置markdown图床-2020-07-18-01-18-20](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-18-20.png)

#### 在vscode的picgo插件中配置github作为图床
1. 在vscode的扩展列表中找到picgo，点击设置按钮 - Extention Settings，会打开设置页面。
![vscode+PicGo+github配置markdown图床-2020-07-18-01-23-31](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-23-31.png)

2. 在设置页面中按照自己的情况填写以下几个设置项
![vscode+PicGo+github配置markdown图床-2020-07-18-01-29-36](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-29-36.png)
至此，可以上传图片到github了

3. 使用快捷命令上传图片
![vscode+PicGo+github配置markdown图床-2020-07-18-01-33-05](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-33-05.png)
以windows系统为例：  
Ctrl + Alt + U：从剪切板上传图片  
Ctrl + Alt + E：从本地选择图片文件上传  
Ctrl + Alt + O：输入图片文件的本地路径上传  
上传完成后，直接生成Markdown的图片链接，可以直接用，很方便：
![vscode+PicGo+github配置markdown图床-2020-07-18-01-58-33](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-58-33.png)

4. 设置重命名图片的名称  
这个设置中说的很明白，直接见截图
![vscode+PicGo+github配置markdown图床-2020-07-18-01-37-15](https://cdn.jsdelivr.net/gh/yuyong1992/picbed/image/vscode+PicGo+github配置markdown图床-2020-07-18-01-37-15.png)
重命名的话，PicGo的客户端支持的更多，支持上传之前手动输入、以及光标提前选中一段文本图片以选中的文本为名称。  
PicGo是github上面的一个开源项目，下载可以见链接：[PicGo](https://github.com/Molunerfinn/PicGo)

#### 踩坑说明
1. 图片上传经常会失败，得多试几次，应该是因为墙的原因  
如果有vpn，那这就不算个问题了
2. 同样因为github访问困难，图片的加载也很慢，此时可以使用jsdlivr  
jsDelivr 是一个提供含JavaScript库、jQuery插件、CSS框架、字体等Web上常用静态资源的免费开源的 CDN 解决方案。其采用全球CDN加速，确保每个地区的使用者都能获得最好的连接速度，  
而在大陆地区使用了国内的CDN加速。因此jsDelivr在大陆也有很好的相应速度，jsDelivr可将不同的JavaScript或CSS libraries集合在一起使用，  
同时，jsDelivr也提供包括npm、GitHub、WordPress等项目的镜像服务。

<hr />