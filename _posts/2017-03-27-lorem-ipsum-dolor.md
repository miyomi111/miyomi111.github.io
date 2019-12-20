---
title: An Intro to Git and GitHub for Beginners (Tutorial)
teaser: Translation project 
category: translation
tags: [new, introduction, translation]
---

### 步骤1： 创建本地git存储库 

使用git在本地机器上创建新项目时，首先要创建一个新 **存储库** (或者通常是'**repo**'). 

要使用git，我们将使用终端。如果您对终端和基本命令没有太多经验，请查看 [本教程](http://mac.appstorm.net/how-to/utilities-how-to/how-to-use-terminal-the-basics/) (尤其是“导航文件系统”和“移动”部分).

首先，打开终端并使用`cd` (更改目录) 命令移动到要将项目放置在本地计算机上的位置.例如，如果桌面上有“项目”文件夹，则可以执行以下操作：

![](https://wx4.sinaimg.cn/mw1024/007awXQDly1ga2z7mcgxrj30ky08vwel.jpg)

要在文件夹的根目录中初始化git存储库，请运行 **git init** 命令: 

![](https://wx1.sinaimg.cn/mw1024/007awXQDly1ga2z7mzf4vj30ki081aa4.jpg)

### 步骤2: 向repo添加新文件

继续使用你喜欢的任何文本编辑器或运行 [touch](http://linux.die.net/man/1/touch) 命令将新文件添加到项目中.

一旦你在包含git repo的文件夹中添加或修改了文件，git就会发现在repo中已经进行了更改。但是，git不会正式跟踪文件（也就是说，将其置于提交中-我们将在下面详细讨论提交），除非你明确告诉它。

![](https://wx4.sinaimg.cn/mw1024/007awXQDly1ga2z7ngmphj30k808kgln.jpg)

创建新文件后，你可以使用该 [**git status**](http://git-scm.com/docs/git-status) 命令查看git知道哪些文件存在。 

![](https://wx1.sinaimg.cn/mw1024/007awXQDly1ga2z7nnvulj30k1082jrf.jpg)

![](https://wx1.sinaimg.cn/mw1024/007awXQDly1ga2z7l4zmvj30jy08ajrf.jpg)

这基本上是说, "嘿, 我们注意到你创建了一个名为mnelson.txt的新文件，但除非你使用'`git add' `命令，否则我们不会对它做任何事情。" 

### 提示：准备环境、提交和用户

你第一次学校git时最困惑的部分之一是准备环境的概念以及它与提交的关系。

**提交** 是自上次提交以来更改了哪些文件的记录。实际上，您对repo进行了更改（例如，添加文件或修改文件），然后告诉git将这些文件放入提交。

提交构成了项目的本质，并允许您在任何时候返回到项目的状态。

那么，你如何告诉git将哪些文件放入提交中？ 这就是 [**准备环境** 或 **索引**](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)的位置. 如步骤2所示, 当你对repo进行更改时，git会注意到文件已更改但不会对其执行任何操作（例如在提交中添加它）。

要将文件添加到提交，首先需要将其添加到准备环境。为此，你可以使用 **git add<filename>** 命令 (请参阅下面的步骤3).

一旦你使用git add命令将你想要的所有文件添加到准备环境，你就可以告诉git使用 [**git commit** ](http://git-scm.com/docs/git-commit)命令将它们打包到一个提交中. 

注意：暂存环境（也称为“暂存”）是新的首选术语，但你也可以将其称为“索引”.