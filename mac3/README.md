有友邻询问，恰巧很多人看不懂第一篇文章。顺便多解释几句几者的关系：

  * brew：Mac下的包管理机制，常用的命令提示符软件，都可以使用它安装。
  * brew cask：基于brew的Mac 程序封装机制，常用的Evernote、dropbox等等均可一键安装。
  * app store：上述两者难以安装的软件，可以通过它来购买或者安装，如keynote等。

为什么要这么来装机？这是转变思维方式的第一步。一行命令能干的事情就交给命令吧。它带来的好处是自动化！

所以，Mac下一键装机的最佳实践即是：

## 安装xcode

在App Store里面免费下载。Apple官方出品。编译下软件与开发mac、ios等软件需要。安装好Xcode之后，打开偏好设置，安装command line tools，如下图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m3-1.png)

## 更改隐私设置与右键设置

Mac默认只能安装授权之后的软件，必须更改设置。如图所示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m3-2.png)

更改触摸板默认设置：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m3-3.png)

设置鼠标右键

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m3-4.png)

## 安装brew

在应用程序=》实用工具中，打开终端，输入命令：

`ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"`

以下操作均继续在终端中执行。

## 安装brew cask
    
    brew tap phinze/homebrew-cask
    brew install brew-cask
    

## 安装brew 基础套件
    
    brew install wget
    brew install curl
    brew install openssl
    brew install imagemagick #未来Rails图片处理需要
    brew install gfortran #未来R语言等编译需要
    brew install node #未来安装Ruby web服务器pow需要
    
    brew install zsh
    brew install git-flow
    brew install python
    

## brew cask安装基础软件
    
    brew cask install google-chrome  
    brew cask install iterm2
    
    brew cask install textmate
    brew cask install sublime-text
    brew cask install textexpander
    brew cask install jumpcut
    
    
    brew cask install the-unarchiver   #解压软件，类似于Windows下的winrar
    brew cask install evernote           #与windows下一样，笔记软件
    brew cask install skitch             #ervernote配套的截图软件
    brew cask install dropbox            #与windows下一样，文件同步软件，你的Windows数据在这里
    brew cask install zotero              #网页收藏与文献管理软件
    brew cask install anki                 #记忆软件
    brew cask install mou                 #Mac独有的写作软件，基于Markdown格式，可导出PDF
    brew cask install virtualbox         #用来跑Windows的虚拟机
    brew cask install alfred               #Mac独特软件，用来帮你快速调用程序与算账
    brew cask install skype
    brew cask install audio-hijack-pro  #录音软件
    brew cask install postgres          #postgresql数据库
    brew cask install self-control      #避免分心的软件
    brew cask install qq                #qq
        brew cask install vlc                #视频软件
        brew cask install rstudio            #R语言开发软件
    

也可以将以上命令精简为：
    
    brew cask install google-chrome   && brew cask install iterm2 && brew cask install textmate && brew cask install sublime-text && brew cask install textexpander  && brew cask isntall jumpcut
    
    brew cask install the-unarchiver && brew cask install evernote  && brew cask install dropbox && brew cask install zotero && brew cask install anki  && brew cask install mou   && brew cask install virtualbox &&  brew cask install alfred &&  brew cask install skype
    

完事！一切就这么简单！

在这个过程中，你可以喝咖啡或者同步dropbox、ervernote、zotero文件去。

## 如何更新已安装程序

在终端中输入：`brew update && brew upgrade`即可。

## 更多

  * [Mac安装软件新方法：Homebrew-cask](http://www.yangzhiping.com/tech/homebrew-cask.html)