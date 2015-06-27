## 温故而知新

在前文开机ABC中，我们侧重介绍了Mac下如何安装新程序、找到自己要的程序，以及如何一键更新。再次重复一下，核心方法是：

1、在终端中输入命令:

一键自动安装你想要的软件，如dropbox、ervernote等等，是：`brew cask install dropbox`这种格式。

自动更新所有的软件是：`brew update`

2、在系统偏好设置，里面，设置后台自动下载更新，如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-1.png)

  * brew足以安装80%的类似于curl、wget、python、R、postgresql、mysql等命令导向的软件
  * brew cask足以安装80%常用的类似于dropbox、evernote、Rstudio等窗口导向的软件
  * 剩下的软件，既不在brew中，也不在brew cask中，如QQ等，则交给app store来下载与管理。

这样你的Mac始终就是保持在最新程序状态，不再需要像windows下那么烦恼去一步一步点击更新程序，即使安装各路软件管理工具，由于Windows自身机制问题，也无法实现全自动地更新。

接下来的这篇，重点介绍的是Mac下的桌面管理，核心点是如何做到保持桌面干净与注意力最大化。让我们先从一个仍然由于内核机制问题，Windows下无法漂亮实现的功能开始。

## Mission Control

参考2009年老文：

> 现代操作系统的多窗口设计，使得人们较易采取一种多线程的处理方式处理任务，比如开着QQ、MSN、Gtalk、skype等聊天工具，同时听着音乐，写着文档。这是互联网时代人们习惯的工作娱乐方式。虽然实践的发展，向人们提出了多线程处理任务的需求，然而，由于Windows下欠缺便捷的、形象的窗口切换工具，使得Windows下，人们较难摆脱多窗口工作情景对人们注意力的干扰。在MAC下，借助苹果公司创新的Spaces功能，可以快速地切换桌面。例如，我们可以开设2个桌面，一个用于处理杂物，在这个桌面下，开着下载、日常沟通、邮件等较容易分散注意力的任务窗口；另一个桌面则专注于创造型任务，比如写作、翻译、编程或者其他视频处理、图像创作等创意工作。在MAC下，这种切换很炫也很自然，更重要的是：实用。

我们要实现的目的是，

  * 第一个桌面上： 开着日常沟通、邮件等较容易分散注意力的任务窗口
  * 第二个桌面上：专注于创造型任务，比如写作、翻译、编程或者其他视频处理、图像创作等创意工作
  * 第三个桌面上：跑着iterm、活动监视器等监察电脑状态或者下载的程序

如何实现？点击Dock下第三个程序：Mission Control

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-2.png)

出来之后，将鼠标甩到右上角去，点击右上角的**新建桌面**，然后就会发现多了个桌面，我们连续新建二个桌面，总计有三个了，如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-3.png)

比如，我们将迅雷分布到第三个桌面上，直接将其拖到桌面3上即可。这样主工作界面，只剩下最专注的，不容易受到干扰的程序。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-4.png)

## Spotlight

它是个类似于Windows下的Google桌面搜索，Mac自带的程序。首先可以在【系统偏好设置】里面，修改它可以搜索的类型与快捷键。

假设按照默认的快捷键呼出，那么，就可以检索全电脑已经索引的资料。如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-5.png)

我们可以发现，它将Mac中所有与TED相关的内容都检索出来了，甚至包括Evernote中的内容！然后将鼠标放在上面，我们可以直接看到全文！

同样，可以通过这种方式，快速呼出你想要的程序。来自第三方开发者的alferd将其发挥到登峰造极的水准。这就是我们要接下来介绍的。

## Alfred

仍然使用：brew cask install alfred ，自动安装好alfred，免费版已经可以拥有强大的快速呼出程序，直接算账的功能，按下alt+空格，

如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-6.png)

它直接在你的当前工作页面弹出相应结果：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-7.png)

今天我要介绍的亮点还不是在这里，而是收费版的工作流功能。大量第三方开发者写了数百个工作流，从而可以一键获得你想要的消息，就像刚才那个计算器一样。他们共享在这里：

  * [Alfred 2 Workflow List | Search, Install and Share](http://www.alfredworkflow.com/)
  * [Share your Workflows - Alfred App Community Forum](http://www.alfredforum.com/forum/3-share-your-workflows/)

比如，传统要在豆瓣查一本书，先是打开浏览器，然后输入豆瓣，再跳到图书，再输入检索关键词。。。现在的步骤则是一键完成。

让我们先从刚才的[http://www.alfredworkflow.com](http://www.alfredworkflow.com/) 网站下载到，完成豆瓣这个任务的相应的工作流，下载地址是：

然后：直接双击下载的workflows文件，或者打开`Alferd=》Preferences => workflows`，将刚才下载的workflow，拖放过来，如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-8.png)

确认**import**，安装完毕。现在我们可以按照作者说明，输入：

`book 社会网络分析`，直接获得结果：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-9.png)

同样的方法，我们可以一键获得当前北京的PM2.5，难怪今天心情不错，难得的好天。。。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m2-10.png)

更多适合国内使用的工作流详情参见：

  * [国人必备的30个Alfred Workflow - Mac软件推荐 | 玩儿法](http://www.waerfa.com/alfred-workflow)

## Mac与Windows的本质差异

通过这三个程序，我们可以重温一下09年的老文：[如何提高创作型任务的效率？（MAC版） ](http://www.yangzhiping.com/psy/mac.html)：

> 因为心理学家诺曼的贡献与苹果在工业设计上的传统优势，Mac与Windows的最大不同是注意力。MACOSX以简洁的设计取胜，甚至强迫用户将注意力聚焦在当前工作之上。Windows系列操作系统设计，相对而言，缺少一个统一并且强硬执行下去的注意力法则。在Windows上，你可以看到大量分散你的注意力的软件设计，同时，在Windows上，格外泛滥你可能只需要20%功能，但是不得不受到其他80%的功能设计带来的诸如升级、数据维护等复杂操作的干扰。苹果公司作为一种与众不同的硅谷精神的“传销”头头，很好地维持了整个MAC生态链对用户注意力的关注，微软在这方面，则逊色较多，在Office系列中的全屏模式，往往你是阅读者而非创作者。

## 小结

我们可以通过Mission Control来将分散注意力的程序给切割开，保持桌面的专注与干净；同样，可以通过系统自带的Spotlight与第三方的Alferd，快速呼出程序、一键获得结果。