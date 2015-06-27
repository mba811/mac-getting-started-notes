## 背景

这是个好时代，原本离我们很远的优质课程垂手可得；这是个坏时代，数字鸿沟渐渐加深。善用网络与沉迷网络，区分开两类人群。

这篇帖子侧重介绍：

  * 有哪些优先级别较高的优质课程？
  * 如何批量下载它们？
  * 如何管理这些优质课程？
  * 如何组建家庭影院播放它们？

其实谈及的技巧，并非Mac不可，在Windows上照样可行。

## 1.有哪些优质课程？

这方面的帖子，我写过太多了，请参考：

  * [不上大学，你可以学些什么？](http://www.yangzhiping.com/psy/open-classroom.html)
  * [如何学习科学：开放科学工具箱](http://www.yangzhiping.com/psy/open-science-toolbox.html)
  * [Ruby视频资料清单](http://www.yangzhiping.com/tech/ruby-casts.html)

重点而言，这些优质课程值得收藏、收藏再收藏：

### 1.1 适合所有人

  * [Coursera.org](https://www.coursera.org/)：名校课程汇集
  * [TED: Ideas worth spreading](http://www.ted.com/)： 尖峰创想，启迪心智

### 1.2 适合开发者或者极客

#### Code School

  * [Learn by Doing - Code School](http://www.codeschool.com/)

应该是我定过的课程中最好的了。比Railscast更系统与更深一点，比peepcode更有趣与更短一些。

#### RailsCasts

  * [Ruby on Rails Screencasts - RailsCasts](http://railscasts.com/)

作者是ruby社区的老黄牛，绝对英雄。坚持了多年，每周一个免费视频。很多人都是通过他的视频入门的。更牛的是，作者一切内容都尽可能开源。

#### PeepCode

  * [PeepCode | Programming and Development Tutorial Screencasts for Web Developers and Alpha Geeks](https://peepcode.com/)

近期刚刚被收购。这个公司出品的教程质量偏高，部分视频有一定难度，介绍的内容，比如Backbone.js，node.js这些，总是先人一步，代表了开发者社区未来的一种倾向。里面的play by play 栏目非常有趣，录制了Zed shaw等世界级优秀程序员实时工作的屏幕。可以看到他们的vim、textmate等等：）

#### confreaks

  * [confreaks.com](http://confreaks.com/)

confreaks是一个录制各个技术大会的网站。包括去年的openstack、历年的Ruby与Rails大会等录制。

### 1.3 适合科研工作者

  * [videolectures](http://videolectures.net/)

众多高质量，包括诺奖得主参与的学术会议视频、ppt合集。也不仅仅是学术会议。包括众多高质量课程。遗憾的是，网站本身对Html5等支持较差，难以通过ios等设备查看。

## 2.如何批量下载它们？

为什么要批量下载？

因为，批量下载有这么多好处：

  * 跨设备同步进展方便，比如，在没有网络的环境下浏览
  * 分享与进一步处理方便
  * 更容易获得随机点播带来的惊喜

我将批量下载它们的方法收集在一个项目中：[ouyangzhiping/metacourse](https://github.com/ouyangzhiping/metacourse)。目前已经添加了批量下载它们的方法：

  * courera
  * railscast
  * TED

未来将补充完善其它优质课程的网站。当然，现在也有更简单的办法，就是使用我已经解析之后的下载源。以广受大众欢迎的TED来举例，如何批量下载。

## 3.如何批量下载一千个TED中文视频

我们的目标是下载一千多个TED中文语言版本的视频，并且文件名最好重命名为作者_演讲标题这种格式。如果是其它语言，方法完全类似。

### 3.1 前提

  * 有迅雷离线账号
  * 有150g以上的硬盘闲置空间

### 3.2 开始下载

下载地址文件：[TED_download.list](https://raw.github.com/ouyangzhiping/metacourse/master/download/TED_download.list)

将其下载下来，然后使用迅雷打开即可。没什么特别需要注意的，小提示：

  * 请务必使用离线与加速功能。这样，你可以享受到我已经加速过的部分视频，其它网友也可以享受到你带来的好处。
  * 将这一千多个视频都保存在一个文件夹里面。

下载好了，效果是这样的：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-1.png)

文件名是：`HonorHarger_2011S-480p-zh-cn.mp4` 这种 `作者_事件_解析度_语种`的命名规律。

## 4.如何管理这些优质课程？

这些优质视频，我们该如何管理它？没有简介，未来如何标记哪个看过、哪个没有看过？

仍然以TED为例。打开iTunes，将我们之前的一千多个批量下载的TED视频导入到资料库中，

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-2.png)

我们发现，所有之前下载的TED视频的文件名全部根据`zh-ch`这个界定，自动更新为中文名称了：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-3.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-4.png)

并且有中文摘要了！

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-5.png)

打开finder，iTunes保存这些TED演讲的文件夹位置，我们发现，一切都变为中文了，更适合小孩与家人一起来看了：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-6.png)

如果需要纯英文版与拿它来作英文学习怎么处理？参考这两个网站的下载源;

  * [TED 高清字幕下载 全集](http://www.11131719.com/)
  * [Download TED talks](http://metated.petarmaric.com/)

## 5. 如何组建家庭影院播放它们？

买一台几百元的apple tv3，直接通过airplay功能投放到电视机大屏幕上即可。步骤如下：

1）在iTunes中，打开家庭共享功能。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-7.png)

2）在apple tv3中，打开家庭共享功能，输入你的iTunes所使用的apple id账号即可。

一切完事！然后可以舒舒服服，坐在沙发上，用遥控器来看自己想看的优质课程。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m6-8.png)

## 6. 其它

以上方法适用于一切批量下载的优质课程，同样，我们还可以直接使用iTunes U功能，即大量优质课程，如TED的itunes u课程尤其值得参与：

  * [creative problem solving](https://itunes.apple.com/us/course/creative-problem-solving/id499099545)
  * [understanding happiness](https://itunes.apple.com/us/course/understanding-happiness/id497857361)
  * [leading wisely](https://itunes.apple.com/us/course/leading-wisely/id512987525)

## 相关

  * [关掉电视，连线世界](http://www.douban.com/note/264824466/)