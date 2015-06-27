音乐与视频，向来Mac擅长，写作与演讲，Mac也擅长。相信乔老爷子的keynote迷倒了不少果粉。只是很多时候，从Windows下转过来的朋友，采取旧思维方式，死抱着Word不放，然后感慨，怎么这么难用。

今天侧重介绍的是四个只有Mac版本的文本高效输入神器。

## textexpander

### 安装方法

在终端中输入：
    
    brew cask install textexpander
    

### 基础设置

将配置同步到Dropbox中，这样，未来在本机设置的tips可以迁移到任何一台电脑。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-1.png)

### 开始使用

示例一：时间与签名的快速输入

比如，作者写邮件时有个小习惯，一般会署上日期，以提供自己时间流逝的飞快。

怎么输入？在任何邮件、任何文本处输入：ddate 即可，它就会自动变为当天的日期。它是怎么实现的？打开 textexpander，如下图所示，设置你的触发键值即可：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-2.png)

同样，在任何文本处输入：`;web` 即可，它就会变为预设的个人网站网址。

示范二：对笔者来说，它不仅仅是一个快速文本输入工具，它更是一个快速记忆库。平时大量经过复核与验证正确之后的命令，都保存在这里。

同样，搭配textexpander更复杂的设置，可以实现更快速地输入输出。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-3.png)

## jumpcut

没什么多说的，一个必不可少的软件。剪贴板管理软件。安装方法仍然是：
    
    brew cask install jumpcut
    

通过它，能够将你的所有粘贴记录保留下来，这样，在处理文本时，极为省事省力。安装好了之后，它会默默保留在界面右上角，记录你的复制记录。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-4.png)

## TextMate

TextMate的安装方法仍然是：
    
    brew cask install textmate
    

通过它的bundle机制，你可以快速了解到一门常见软件的核心语法与核心机制。比如，以下就是Markdown的核心语法与核心功能：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-5.png)

通过它的跳转，可以快速在长文档中切换。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-6.png)

所以，TextMate不仅仅是一个文本编辑工具，它对我来说，更是一个快速了解任何一门编程语言与处理长文本的利器。更多参见图书：

  * [Textmate](http://book.douban.com/subject/1908201/)
  * [如何学习一门新的编程语言？](http://www.yangzhiping.com/tech/learn-program-psychology.html)

## Markdown粘贴利器

虽然 textexpander，可以实现大量Markdown以及任何一种文本格式的快速处理，如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-7.png)

不过如果仅仅是整理网页信息，还有更简单的处理方式，安装Chrome插件：

＊ [Chrome 网上应用店 - Copy as Markdown](https://chrome.google.com/webstore/detail/copy-as-markdown/fkeaekngjflipcockcnpobkpbbfbhmdn)

这样，在你希望引用的网页上粘贴以下，就会自动补齐为Markdown的引用格式，非常有利于快速整理网页信息。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-8.png)

## Mou

这个介绍过很多次了。。。没必要介绍了吧。安装方法仍然是：brew cask install mou。更多介绍参考之前老文。秀一秀作者寄过来的MouStand：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m4-9.png)

一篇关于作者的采访：

  * [獨立開發者的孤獨——Mou 作者羅晨專訪 - Inside 硬塞的網路趨勢觀察](http://www.inside.com.tw/2013/07/19/mou-creator-chen-luo-interview)

## 小结

在Mac下，我们可以通过textexpander来定义一切需要重复输入的大段文本、信息等；可以通过 jumpcut来保存复制粘贴历史记录；通过TextMate来处理一切文本与快速掌握一门新的编程语言要点。