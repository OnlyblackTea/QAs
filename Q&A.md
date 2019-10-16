<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Git部分](#git部分)
  - [git是什么？](#git是什么)
  - [如何使用git？](#如何使用git)
    - [git bash的安装](#git-bash的安装)
    - [git bash的使用](#git-bash的使用)
      - [git bash和VSCode的关联](#git-bash和vscode的关联vscgitmd)
      - [创建代码仓库，并向你的代码仓库提交修改](#创建代码仓库并向你的代码仓库提交修改)
    - [在github创建分支](#在github创建分支)
- [Markdown部分](#markdown部分)
  - [Markdown是什么？](#markdown是什么)
    - [基础语法（来自MPE介绍页面  ）](#基础语法来自mpe介绍页面-2)
- [Ubuntu的安装](#ubuntu的安装)
  - [WSL的安装方法](#wsl的安装方法)
  - [虚拟机中的安装方法](#虚拟机中的安装方法)
  - [docker中的安装方法](#docker中的安装方法)
  - [服务器的租借与使用](#服务器的租借与使用)
- [C++部分](#c部分)
  - [Visual Studio Code的安装与使用](#visual-studio-code的安装与使用)
    - [安装](#安装vsc的安装md)
    - [使用](#使用vsc的使用md)
- [控制台相关](#控制台相关)
  - [控制台界面介绍](#控制台界面介绍)

<!-- /code_chunk_output -->

# Git部分
## git是什么？
> 参考链接：https://www.liaoxuefeng.com/wiki/896043488029600/896067008724000

该链接里用了一个例子很形象地说明了为何人们需要git。

## 如何使用git？
> 参考链接：https://www.liaoxuefeng.com/wiki/896043488029600

鉴于上述链接中的内容过多，同学们在快速掌握git的使用方法上可能会存在困难，下面介绍一些简单的操作及git命令，帮助同学们快速上手。

### git bash的安装
git bash是shell [^1] 的一种，它是github配套的控制台，我们用它在自己电脑上管理版本库。首先去[官网](https://git-scm.com/)下载。（一般在网站上**download**指向有关下载的页面，对于掌握英语的同学们来说，在该网站上下载git bash不是难事，此处希望大家**各凭本事**）然后执行安装文件，一般来说除了安装地址（**不建议安装在C盘**）以外只需要默认即可。建议大家**仔细阅读**安装文件上的说明，如果有其他需求或者疑问，在**微信群**提出，或者在github上提交**issue**，我们会在此处更新答疑。
### git bash的使用
> 参考链接：https://blog.csdn.net/sun_life_/article/details/82847801

该文章将git bash从安装后到使用的步骤以图文的形式详细讲解了一遍。
#### [git bash和VSCode的关联](VSCgit.md)

#### 创建代码仓库，并向你的代码仓库提交修改
在安装时选择以vscode作为git bash的编辑器，vscode中会出现“源代码管理”页面。在其中可以进行可视化的版本库管理，不过我们接下来介绍终端中的方法
git bash安装完毕以后，在vscode的终端（默认为powershell）中输入git，会输出git自带的指令列表，其中简单地介绍了git命令及参数，我们选其中一部分来讲解。
* 首先确保你有一个[github](https://www.github.com)账号，然后我们开始
```bash
$ git config --global user.name "YOURNAME"
$ git config --global user.email "EXAMPLE@EXAMPLE.COM"
```
其中$表示一行输入的开始，请把引号中的部分改成你自己的用户名和邮箱。
* 克隆（下载）一个版本库
```bash
$ git clone https://www.example.com
```
* 或者创建一个版本库
```bash
$ git init
```
只要使用该命令，终端就会把当前目录创建为一个版本库。但是还没结束，如果你想要创建一个远程版本库，首先在[github](https://www.github.com)上创建一个新的repository，然后repository name与你的版本库文件夹保持一致，其他不变，直接点击create repository，然后github会出现一个页面，引导你将本地的版本库上传至远程。
* 在你修改完文件以后依次使用如下命令
```bash
$ git add EXAMPLE.example(你的文件名及扩展名) //添加该文件到版本库
$ git commit -m "备注信息"  //添加备注
$ git push origin master  //推送至github
```
* 你需要善用的控制台命令
```bash
$ dir或ls //查看当前目录下的文件
$ cd //进入某个目录
$ cd ..//回到上个目录
$ mkdir //新建目录
```
### 在github创建分支
> 参考链接：https://www.liaoxuefeng.com/wiki/896043488029600/900003767775424

在上面我们已经介绍了向github上传文件和从github下载文件的操作，而在这个部分中，你将学会如何参与编辑别人的项目。（强烈建议先看参考链接）

以[本项目](https://github.com/OnlyblackTea/QAs)为例子，你可以在这里尝试如下操作：
首先**clone**本项目到你的电脑中，在**终端**中打开该文件夹，输入：
```bash
$ git branch
* master
```
(若不带"$" 则说明不是你将要输入的内容)
其中**master**就是你当前版本库的分支。
输入：
```bash
$ git branch exp
$ git branch
  exp
* master
```
# Markdown部分
## Markdown是什么？
Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。它的功能类似word文档，写法类似html，是一种方便好用的文档整理工具。

### 基础语法（来自MPE介绍页面 [^2] ）

*这会是 斜体 的文字*
_这会是 斜体 的文字_

**这会是 粗体 的文字**
__这会是 粗体 的文字__

_你也可以 **组合** 这些符号_

~~这个文字将会被横线删除~~
```
*这会是 斜体 的文字*
_这会是 斜体 的文字_

**这会是 粗体 的文字**
__这会是 粗体 的文字__

_你也可以 **组合** 这些符号_

~~这个文字将会被横线删除~~
```
当然，Markdown同样可以兼容LaTeX等工具，来表达数学公式，你甚至可以用Markdown来写你的论文。不过，即便它如此受欢迎，它依然存在很多问题，尤其是兼容性和语法格式标准等问题，遇到的时候还是很困扰的。
虽然如此，只要深入研究，你会对它爱不释手的。

# Ubuntu的安装

## WSL的安装方法



## 虚拟机中的安装方法

## docker中的安装方法

## 服务器的租借与使用

# C++部分

## Visual Studio Code的安装与使用

### [安装](VSC的安装.md)

### [使用](VSC的使用.md)

# 控制台相关

## 控制台界面介绍

[^1]: 在计算机科学中，Shell俗称壳（用来区别于核），是指“为使用者提供操作界面”的软件（命令解析器）。它类似于DOS下的command.com和后来的cmd.exe。它接收用户命令，然后调用相应的应用程序。(来自百度百科)

[^2]: [MPE介绍页面](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn)，Markdown Preview Enhanced 是一款为 Atom 以及 Visual Studio Code 编辑器编写的超级强大的 Markdown 插件。 这款插件意在让你拥有飘逸的 Markdown 写作体验。