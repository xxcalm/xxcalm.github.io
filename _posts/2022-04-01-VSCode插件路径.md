---
layout: post
title: VSCode插件
descripyion: 修改VS Code插件的默认位置
date: 2022-04-01 
tag: VSCode
---

# VSCode插件

**VSCode插件默认存放位置在C盘下：**

C:\Users\username\\\.vscode\extensions

插件少的时候三四百MB，多的时候红盘警告，由于VSCode没有提供设置插件的存放位置，所以这里提供一个可行办法：

**1.新建一个文件夹用于存放你的VSCode插件：**

如`D:\VSCode\extensions`

**2.在cmd修改插件安装位置**

输入：code --extensions-dir 目标文件夹，然后enter，注意：目录一定要用引号括起来

如` code --extensions-dir "D:\VSCode\extensions"`

此时如果用VSCode的快捷方式打开，会发现并没有生效

**3.修改快捷方式**

右击VSCode快捷方式，选择属性，找到**目标(T)**在里面追加以下内容

`--extensions-dir "D:\VSCode\extensions"`

注意：是追加！不是修改！

此时就配置完成啦，但是新建的extensions文件里面什么都没有，自然你现在VSCode的扩展也没东西，你可以重新下载，完成之后，原来C盘的extensions文件也没用了，你可以选择性删除。
