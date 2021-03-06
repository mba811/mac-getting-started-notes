## 背景

一直觉得，在办公室办公是一件非常不人道的事情。一天8个小时，呆在一个狭小空间内，对着一个屏幕。嗯，还很有成就感。在古代或者未来，这叫坐牢；在今天，这叫白领啊。5*8工作制度，并不是为今天互联网时代设计，而是沿袭工业革命的泰勒实验而来。它没有考虑到众多今天时代的特点：1）城市日益恶劣的交通；2）工作家庭平衡；3）办公室无数杂音的干扰；4）需要自我决定与创作的知识工作者的普及。

所以，我个人工作习惯是周一、二去公司，周三休息，周四到周日在家工作，周六休息。为什么周三休息？周三是一个承前启后，最容易低谷的一天。将其设为休息日，则可以利用自我决定论的周末效应，即在休息日反而能够解决工作日解决不了的难题。

我相信，未来远程办公的人会越来越多，今天重点聊聊互联网背景之下，Mac的远程协作。

## github：远程协作基石

这个不用再多说了，请参考去年的老文章：[如何高效利用GitHub](http://www.yangzhiping.com/tech/github.html)

### 安装与配置

更简单的办法是：
    
    brew cask install github
    

然后通过界面进行同步与提交。

上周末，给友人们简单演示了一下如何通过它创建一个博客与一个项目，请格外记住，github与git模式并不仅仅适用于编程，它适用于一切远程协作的模式！通过与Service Hooks的配合，在无数第三方应用的配合之下，它几乎支持一切你能想到的最佳远程协作方式。以下，让我们以hipchat为例。

## hipchat：隐私群聊工具与工作记录薄

什么是[hipchat](https://www.hipchat.com/)？它是一个隐私的群聊工具，支持Mac、Windows、Web与手机等众多终端。但是与传统企业QQ等不一样，由于它自身的开放气质，支持无数第三方API，以致它已成为开源界与远程开发标配之一。

远程协作时，经常由于不清楚同事的进展，也不清楚同事的需求。此时，使用hipchat，创建一个隐私房间，将项目成员拉入进来。

这样，就相当于一个虚拟办公室有了！更重要的是，它是异步的！你并不需要实时处理同事的信息！

重点来了！由于hipchat非常开放，它同样支持无数第三方api，这样我们将一切信息写入到hipchat的房间里面。举个实践小例子。如何配置github的提交信息，比如，我写了一段代码或者一篇文章，同事马上收到？

步骤如下：

1、注册hipchate账号，并创建房间。假设你的房间叫做：project1。

2、打开github的Service Hooks，详细文档参考：[Repo Hooks | GitHub API](http://developer.github.com/v3/repos/hooks/)

如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m5-1.png)

我们可以看到无数第三方git hook，现在，让我们找到hipchat。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m5-2.png)

然后填写房间号与授权信息即可。Room（房间号）填入project1；（授权码）去这里找：

  * [HipChat - API Tokens](https://www.hipchat.com/admin/api)

然后勾上`Notify`、`Active`即可。大功告成！

未来，我们在房间里面，会看到任何与该github项目相关的提交、评论等信息，这样同事之间不用反复通知与确认。

## droplr：截屏快速分享

[Droplr](https://droplr.com/hello) 是与hipchat的一个绝配。假设，你这边有什么截屏发给同事的。直接截屏，它将立即自动上传并生成相应网址。

将该网址复制到hipchat的房间聊天记录里面，会自动出现相关图片。同样，它不仅适用于与hipchat的搭配，也是一个很好的图床。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m5-3.png)

## dropbox与迅雷：大文件快速分享

dropbox没什么多介绍的，直接利用共享文件夹即可，如是团队协作建议购买企业账号。迅雷则主要利用它的迅雷离线与快存功能，这样可以快速将上G或者几十G的大文件分享给远程同事。同样，如是团队协作，建议留意迅雷即将推出的企业账号功能。

与迅雷在windows下的臃肿相比较，在Mac下，它精简得都不太像是迅雷了。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m5-4.png)

## 小结

远程协同工作，我们可以通过git或者github为基础，搭建一个隐私的项目hipchat房间，将项目相关信息，全部投射到该房间上来，以方便全文检索与实时通知；借助droplr，可以快速分享小文件与截屏等、借助dropbox与迅雷，我们可以快速分享大文件。