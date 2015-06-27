## 开机之前的准备工作

A1. 需要准备一个Apple ID账号，它是干嘛的？用于同步iphone、Mac之间的数据，如日历等。如果常用邮箱是QQ邮箱，那么，还会同步QQ上的备注信息。

在`苹果键＝》系统偏好设置 ＝》iCloud` 查看，多数需要更改的个人设置习惯也是在这里修改：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-1.png)

## 之前的Windows老数据怎么办？

A2. 三种方法同时备份最靠谱。

1）最简单的办法是购买一个Dropbox年费账号，100G左右空间，可以同步多数常用资料。先将其安装在Windows上，再将其同步过来。Dropbox的工作极其自动化，它在电脑的右上角：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-2.png)

要切换输入法、查找文档、加入Wifi、调节音量，也都是在右上角这里执行。

2）使用Vmware fusion迁移助理，将之前的Windows笔记本的所有程序与数据，迁移为一个虚拟机。

迁移助理下载地址是：[http://www.vmware.com/go/pc2mac](http://www.vmware.com/go/pc2mac)

未来如果有特殊程序必须使用Windows，随时可以启动它。是一个下图最右边这样图标的程序：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-3.png)

3）再使用移动硬盘备份一下老数据。怎么调出移动硬盘？点击底部的Dock，Dock的第一个程序就是Finder（Mac下的资源管理器），然后再查找设备，就可以看到。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-4.png)

Dock的概念，类似于Windows的程序快捷菜单，你可以点击右键设置是否保留在这里：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-5.png)

三管齐下，在线同步、虚拟机调用程序与移动硬盘查看。足以冗余可能出现的问题。

## 密码与使用习惯如何迁移

A3. 常用密码使用密码管理软件，如LastPass等。浏览器使用Chrome、输入法使用Windows上最常见的搜狗输入法，这样迁移习惯较快。打开你的Dock上的Chrome，找到右上角的LastPass，它就是用来保存密码与自动登陆网站的：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-6.png)

另外有一些，有助于迁移Windows使用习惯的好方法是，尽可能使用在线软件。预装的Chrome插件：

  * [Chrome 网上应用店 - LastPass Vault](https://chrome.google.com/webstore/detail/lastpass-vault/ncliohomlfopnmlfkepkcbnhmeijkhhf)  

  * [Chrome 网上应用店 - Copy as Markdown](https://chrome.google.com/webstore/detail/copy-as-markdown/fkeaekngjflipcockcnpobkpbbfbhmdn)  

  * [Chrome 网上应用店 - Markdown Here](https://chrome.google.com/webstore/detail/markdown-here/elifhakcjgalahccnjkneoccemfahfoa)  

  * [Chrome 网上应用店 - 印象笔记·悦读](https://chrome.google.com/webstore/detail/clearly/iooicodkiihhpojmmeghjclgihfjdjhj)

更详细的新手迁移常见问题参考Apple官方文档：

  * [Apple - 你会爱上 Mac 的理由 - 解答你遇到的问题](http://www.apple.com.cn/why-mac/faq/)
  * [Apple - 支持 - OS X Mountain Lion - 应用软件](http://www.apple.com.cn/support/osx/applications/)

或者：

  * [从 Windows 到 MacOS X 完全搬家手册 - 通天塔](http://t.tt/37/)

## Q4. Mac有什么Windows一定办不到的事情

A4. time machine。自动备份数据的两种方法：

  * 将Mac连接到支持Time machine的无线路由上，它会自动备份数据。  

  * 接上设置好的移动硬盘，它也会自动备份。备份进展，在右上角的菜单栏查看。  


![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-7.png)

更多参见：[Mac 基础知识：Time Machine](http://support.apple.com/kb/HT1427?viewlocale=zh_CN)

## 怎么安装软件？

Windows与Mac的软件包机制极其不同。Mac下的软件后缀为app，所有软件相关的数据都包裹在这一个文档里面。你可以点击右键，**显示包内容** 查看更具体的内容：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-8.png)

Mac下安装软件的传统方法是，

  * 下载后缀为dmg的压缩包文件，解压之后，将里面的app文档拖放到应用程序目录；
  * 另一个类似于Windows的方法是下载后缀为pkg的可执行文件，一步一步确认安装。

使用习惯更好的方法是：

1）常用的软件，可以去App Store中找。它会自动安装。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-9.png)

2）一些基础软件，使用brew与brew cask统一管理。参考我的列表：
    
    brew cask install the-unarchiver   #解压软件，类似于Windows下的winrar
    brew cask install evernote           #与windows下一样，笔记软件
    brew cask install dropbox            #与windows下一样，文件同步软件，你的Windows数据在这里
    brew cask install zotero              #网页收藏与文献管理软件
    brew cask install anki                 #记忆软件
    brew cask install google-chrome  #与windows下一样，已同步Windows上的书签
    brew cask install mou                 #Mac独有的写作软件，基于Markdown格式，可导出PDF
    brew cask install virtualbox         #用来跑Windows的虚拟机
    brew cask install vagrant            #用来在后台跑Windows的虚拟机
    brew cask install alfred               #Mac独特软件，用来帮你快速调用程序与算账
    

如果未来想找一些新的软件，可以去这里先翻翻：

  * [cask列表](https://github.com/phinze/homebrew-cask/tree/master/Casks)

参考文档：

  * [Mac安装软件新方法：Homebrew-cask](http://www.yangzhiping.com/tech/homebrew-cask.html)
  * [Mac开发者2013年新机设置参考](http://www.yangzhiping.com/tech/mac-dev.html)

一些常用的软件，比如 Evernote、Dropbox均可通过它来一键安装。

## 如何更新软件？

1）如果需要更新软件，可以在App Store点击全部更新，它会在后台自动更新下载的软件。

2）与在终端中输入：
    
    brew update && brew upgrade
    

它会自动更新下载的所有软件。

## 怎么这个Windows下常用的软件又找不到了呢！

Windows与Mac有个极大的不同，对于一些自动化、重复性的工作，开发者并不倾向于写一个Windows界面的软件去实现它，而是写脚本去实现它。

碰到的常见问题，如果找不到软件，请找脚本。一般常用的脚本与问题，都能免费下载到。

＊ [Frequent Questions - Ask Different](http://apple.stackexchange.com/questions?sort=frequent)

当然，如果还是特别习惯Windows下，缺功能先找软件的习惯，这些网站，可以去找：

  * [Mac软件推荐 | 玩儿法](http://www.waerfa.com/)
  * [The Setup / Interviews](http://usesthis.com/interviews/)
  * [新工具](http://xingongju.com/)
  * [The Setup](http://setup.xiuxiu.de/interviews/)
  * [V2EX › MacBook Air](http://v2ex.com/go/mba)
  * [V2EX › Mac OS X](http://v2ex.com/go/macosx)
  * [V2EX › MacBook Pro](http://v2ex.com/go/mbp)

## Q8. 怎么用网银？

  * 京东可以直接使用信用卡快捷支付
  * 支付宝一般没问题，但储蓄卡充值流程大有问题，一个办法是直接刷拉卡拉，手续费高，1%；一个是繁琐的流程，先启动虚拟机，充值之后，再回到Mac下。
  * 企业银行都不支持Mac，需要启动虚拟机。有两个虚拟机，一个是之前数据备份的老Windows；一个是全新的，只装了常用网银的虚拟机。

## 常用软件

  * word使用习惯与windows下几乎一样，但不建议使用，建议改使用其它文档软件，如Scrivener、TextMate、Mou等。
  * ppt请使用keynote，请使用另行采购，已安装的模版
  * Excel仍可正常使用
  * 照片：仍然可以使用Picasa导入与管理照片
  * 截图：请使用Evernote配套的截图软件，在屏幕右上角
  * 音乐：豆瓣音乐支持太差，请使用QQ音乐
  * 输入法：为了使用习惯迁移快，可以使用QQ输入法
  * QQ：没有远程协助功能，但也少了无数广告
  * 下载：仍然可以使用迅雷，离线下载已支持

## 快速掌握Mac程序的方法

  * ps1： [2011年Mac新手培训](https://speakerdeck.com/zhiping/2011nian-macxin-shou-pei-xun): 2011年的培训，主要是快速上手软件的方法没过时，其它均已过时

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-10.png)

## 小结

参考老文[如何提高创作型任务的效率？（MAC版）](http://www.yangzhiping.com/psy/mac.html):

> MAC OSX是苹果公司设计开发的一款广受好评的操作系统。如果尝试总结MAC与Windows最大的差异，或许关键字在于：注意力。无论如何，MAC为人们创造了一个新的创意环境，值得你去关注与尝试:D

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m1-11.png)