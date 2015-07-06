# Marboo发布博客，就这么简单

[Marboo](http://marboo.biz/) 从v0.4版开始，新增了一个功能：Make/Rake Button。

点击这个按钮就会触发make或rake命令，执行Makefile或Rakefile中的操作。

通过对Makefile或Rakefile进行配置，可以实现一键式自动发布博客到GitHub/GitCafe，farbox等。

amoblin使用Jekyll来生成静态博客，所以下面以Makefile + Jekyll为例来演示：

## 发布到FarBox

在需要发布的目录下新建Makefile文件，写入如下内容：
    
    default:
        jekyll . ~/Dropbox/Apps/FarBox/markbook
        curl http://farbox.com/service/sync/dropbox/1234567
    

注意第二行jekyll前面不是空格，而是tab符。

第三行是 [手工同步FarBox](http://farbox.com/docs/sync.md) ， 最后的数字替换为你的Dropbox ID。

这里将当前目录下的文件全部导出为html，保存到FarBox下markbook目录中。

这样每次点击MakeRake Button就会更新Farbox下markbook目录中的内容。此时你会发现dropbox开始同步啦。

## 发布到GitHub

GitHub/GitCafe的发布需要使用git，我们先对博客的git库进行一下配置。

进入博客目录，设置工作树路径：
    
    $ git config core.worktree ~/Dropbox/Apps/FarBox/markbook
    

现在git库管理的目录就从当前目录变为FarBox下的markbook目录。

把所有文件都提交，推送到github：
    
    $ git add -A
    $ git commit -m "updte blog"
    $ git push
    

接下来就很简单了，和 [发布到FarBox](http://amoblin.marboo.biz/2013/01/24/markbook-to-farbox.html#farbox) 一样，Makefile文件写入如下内容：
    
    default:
        jekyll . ~/Dropbox/Apps/FarBox/markbook
    cd /path/to/yourname.github.com; git add -A; git commit -m "updte blog"; git push
    

把上面的路径改为自己的git库地址。

这样每次点击 MakeRake Button 不仅会更新Farbox下markbook目录的内容，而且还会推送到github。

MarkBook会等待make结束才有响应。 所以如果文件比较多的话，界面会有短暂的停滞(刚开发出来，急于给大家分享，后期版本会修复)。

发挥你的想象力，看看除了 [`MarkBook Gallery`_](http://amoblin.marboo.biz/2013/01/24/markbook-to-farbox.html#id3) 列出的以外， 还能怎么折腾？

* * *

如果你打算用MarkBook来发布博客，希望能在jekyll模板中增加MarkBook的链接，谢谢！

## Docutils System Messages

System Message: ERROR/3 (<string>, line 74); _[backlink](http://amoblin.marboo.biz/2013/01/24/markbook-to-farbox.html#id4)_

Unknown target name: "markbook gallery".

  

