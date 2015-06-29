# 最佳应用

**Mac-神器**   

#### Alfred

一款几乎所有人都会说是神器的软件。Alfred强化了spotlight，不仅可以快速的搜索本地文件，还可以搜索各种网络上的内容，同时也可以实现完全的键盘操作。真正做到快速启动的同时，也支持自定义各种插件，使其无比强大。可以用来查找文件，直接打开文件或者应用，可以直接进行google搜索，可以查询各种词典，可以查看历史剪贴板……如图是用一个豆瓣插件直接去豆瓣搜索电影。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/Alfred/Alfred.png)

#### Dash

[dash](http://kapeli.com/dash)主要是一个API文档浏览器。可以快速地查阅各种技术的api文档，非常方便。特别是离线环境下，尤其有用。dash还可以存储常用的代码片段以供使用。[![](http://foocoder.com/images/mac/dash.png)](http://foocoder.com/images/mac/dash.png)

#### popClip

[popClip](http://pilotmoon.com/popclip/)也是一个可以提升效率的工具。在你选择文本之后,popClip会弹出，如图所示：[![](http://foocoder.com/images/mac/popClip.png)](http://foocoder.com/images/mac/popClip.png)

可以看到能对选中的文本进行复制，加双引号，打开dash搜索，发微博，添加到things等等。很多功能都不是默认的，和Alfred一样，popClip支持自定义插件。可以在[这里](http://pilotmoon.com/popclip/extensions/)下载各种插件满足不同的需求。 非常强大。

Hazel、Alfred、TextExpander、LaunchBar、PopClip还有Dropzone，相比大家对这些应用应该都非常熟悉吧。你或许都知道这些应用能干什么，但是当你想作一个工作流的时候却往往不知道该用哪一个软件来完成。

同样的工作或许这些应用都可以完成，比如说你要创建一个输入补全，你可以使用TextExpander或者Keyboard Maestro来完成，如果你想将创建一个图片格式转换的工作流，你可以选择使用Automator或者Hazel。那么问题来了！

**你究竟该用哪个应用来完成呢？**

**这要看你用什么触发器了。**应用或许是多种多样的，但是触发器就那么几种，你是想在一个文件放入特定文件夹的时候运行脚本呢？还是想当你打开终端的时候运行？或者在你输入特定的词来触发？在你想要作你自己的工具之前你首先要明确你要用哪种触发器。 
  
下面我介绍下比较常用的几种触发器：   
  
**基于语句的**   
  
  
语句是最为灵活的触发器，Spotlight就是语句触发器的最好事例。比如我想将美元转换到日元，我只需要在Spotlight中输入20 USD to JPY就可以了。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_0ea9a205070a40a.jpg)

Alfred、LaunchBar还有系统自带的Spotlight都属于这个范畴，你可以用于查词，汇率转换，搜索信息等。像Alfred、LaunchBar这些应用还允许你的在搜索结果中重命名、移动或者处理文件。有了Alfred的Workflows(工作流)，你还可以进行如对图像进行优化或者修改大小等操作。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_501d5fdc265bf8a.jpg)

基于语句的触发器之所以灵活的主要原因是他不需要记忆任何快捷键。当我想关机的时候，我只需要输入shutdown就可以完成了。而且这种情况下就不会存在什么快捷键冲突的问题，你可以使用为不同的任务定义相同的语句触发器，比如说一个Alfred Workflows，它的关键字是tb <command>，我并不需要记住所有的命令，只需要记住tb然后在Script Filter中选择我要的命令就可以了。   
  
**基于目录和文件事件的**   
  
  
我们经常要根据不同的文件和目录情况来做出不同的行为，比如把含有指定词语的文件存入印象笔记、给“下载”文件夹下的文件按一定格式进行重命名、删除存放入“废纸篓”中超过三天的文件。但是如果这些能让电脑自己自动完成就更好了。   
而Automator和Hazel这两个应用就可以完美的完成这些。   
Automator是OS X系统自带的应用，用于制作自动化处理工作的工作流、应用或者系统服务。除此之外它还有一个基于目录和文件事件的触发器，就是**Folder Action**。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_08e0c3d9a03e77f.jpg)

Folder Action会自动的监测并你定义的工作流来处理那些被存放入的文件和文件夹。你可以重命名它们，将图片转换成不同的格式，或者提取PDF文件中的文字并保存到另一个文档中。支持Automator的应用也会自动将它们定制好的动作行为列入Automator的可用行为中。例如，如果你有Pixelmator这款软件，你就可以在你的工作流中使用其提供的给图片自动添加水印的功能。如果你对Automator感兴趣，可以再下面**留言**，我会在以后在涵盖一些。   
Hazel在这方面的处理能力则更加强大，你可以用它来设定一系列的规则来匹配被存放的文件名称的模式、最后编辑日期以及文件的内容。它还具有很多其它默认功能如重命名、将匹配的文件整理排序存放入不同的子目录中。你也可以选择对各个匹配文件执行预制的shell脚本、AppleScript或者Automator的工作流等等，比如可以用它来整理并为照片排序、整理收集的截图以及远程执行Keyboard Maestro录制的宏。   
总而言之，如果你想做关于文件或目录行为的工作流，那么你就应该选择Folder Action或者Hazel，这样能为你省去更多的时间。   
  
**特定字串触发的**   
  
这种触发器是在你输入特定字串的时候触发的，使用这种触发器的工具主要由两个：TextExpander和Keyboard Maestro。   
我们先说TextExpander，如果你想做一个快速输入特定格式的文本，那么你首选的应当是TextExpander。虽然Keyboard Maestro也能做到这一点，但是TextExpander是专为这个功能而设计的，所以TextExpander在表现上会更加好。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_1b02b2236861fe5.gif)

TextExpander的特色功能之一是可以弹出一个弹窗来便于你定制更加复杂的输入类型。   
另一点，TextExpander支持富文本的插入，因此你可以定制它自动输入的文本的颜色、字号、或者图片等都可以。如果你对AppleScript或者Shell脚本有所了解的话，你还可以控制TextExpander中输出的值。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_4fba39896130c55.gif)

在其他非自动填充文本的情况下，你就应该用Keyboard Maestro，比如说你可以做一个宏来在你输入.rename的时候来为当前打开的文件进行重命名。这并不是说你不能用Keyboard Maestro来快速输入文本，只是TextExpander在这个方面做得更好而已。   
  
**基于文本选中触发的**   
  
根据你喜欢选择文本的形式，你应该使用的工具也是不同的。   
如果你平时经常使用鼠标或者手写笔，那么你就应该使用那些不需要键盘就可以完成你想要完成工作的工具，比如说你在iPhone或iPad上复制粘贴文本，就只有手指就可以完成。这样说你们应该也知道我要说的就是PopClip了，这款应用就是仿照iOS系统文本选择的浮窗，在里面置有一系列的执行命令，你只需要选中文本，然后再点击命令就可以了。这个工具最常用的地方就在与它的复制粘贴功能，除此之外，他还有非常多的扩展来满足你的其他需求，比如你可以用鼠标选中文本，然后点击命令来自动在Google中搜索、自动将其改成首字母大写的形式或者将选中的文本保存到你的印象笔记中。   


![](http://appwen.com/res/images/blank.gif)

当然不是所有人都喜欢使用PopClip，比如我平时更喜欢使用键盘而不是鼠标，就不怎么使用这种工具。键盘流的用户通常更喜欢使用⌘+⇧+方向键来选中文本，这种方式选中文本的则应该使用系统自带的Automator的服务功能，或者Keyboard Maestro，还有Alfred。   


![](http://appwen.com/res/images/blank.gif)

比如说Brett Terpstra做的SearchLink这个就可以让你在选中文本后，通过你指定的快捷键，比如用⌘+⇧+S，来将它自动变成Markdown格式的链接，非常方便。   
当然这里没有什么规定，你应该用什么工具。每当我想自己做个工具来处理我选中的文本的时候，我首要会选择使用Keyboard Maestro，因为它自带很多快速操作剪切板的功能。但是如果发现一些非常好的其他工具，比如说Alfred上的QuickCursor，我也会使用Alfred来完成一些工作。   
  
**基于文件选中触发的**   
  
你或许会想要一个工作流来完成将你选中的一系列文件传送到FTP服务器上，或者将选中的一系列图片转换成另一种格式。Alfred用户可以直接使用其自带的文本选中这个批处理功能，而通常情况下用户们更喜欢在Finder中选中这些文件并使用Automator来进行文件批处理。当然你还有其他的选择，比如说Dropzone。   


![](http://macgg.b0.upaiyun.com/attachment/thumb/1412/thread/14_2427_65ab47483b75947.jpg)

它具有和DragonDrop同样的功能，可以作为一个临时的文件夹，把你想要移动的文件先放入其中。另外你可以制定一些行为，比如说你可以将一个文件丢到“分享到Dropbox”这个行为上，然后他就会将文件保存到你的Dropbox共享文件夹中，并把分享的链接保存到你的剪贴板中。你可以在其中定制你自己的FTP或者Amazon S3服务器来随时的上传你的文件   
  
**其他事件触发器**   
  
剩下还有很多各种各样的触发器，其中Keyboard Maestro涵盖我个人认为是最丰富的，可以监测当前连接的是什么网络、当前电脑的名称以及当前屏幕的状况(如分辨率)。基本上你所需要的Keyboard Maestro都会有所涵盖，但是这样通常在你所需要的触发器在其他工具中也有的情况下，可以优先选择其他工具，只有在其他工具都无法完成的情况下在选择Keyboard Maestro。   
比如说我有一个宏用于每40分钟监测一次电池剩余电量，这种循环的任务使用其他工具就很难做到，即使能做，估计也需要一些非常复杂的脚本来完成。因此最后我选择使用Keyboard Maestro来完成这个工作，每40分钟获取当前剩余电量的百分比，然后如果低于40%的时候提示我剩余可用时长。   
另一个我经常用Keyboard Maestro的地方就是当我需要模拟一些用户行为的时候，比如说鼠标点击事件、将某个文件放入另一个文件夹中或者自动输入输入钥匙串中的密码等等。Keyboard Maestro的控制流列表中包含很多控制行为，让你的脚本可以根据一些环境变量来自行决定是否该运行脚本，而不需要你自己写代码来定义。   
  
**写在最后**   
  
如果你对Alfred、Keyboard Maestro、Automator或者AppleScript感兴趣，可以在下方留言，我以后会提供更多的相关资料和技巧。另外在本文中提到的几个工作流或者扩展内容也会在近日内翻译出来。   
本文提到的一些效率应用：   
- PopClip [官方网站](http://pilotmoon.com/popclip/) [本站下载](http://appwen.com/read.php?tid=832&fid=28)   
- Alfred [官方网站](http://www.alfredapp.com/) [本站下载](http://appwen.com/read.php?tid=140&fid=28&page=1)   
- Keyboard Maestro [官方网站](http://www.keyboardmaestro.com/)  [本站下载](http://appwen.com/read.php?tid=910&fid=28)   
- Hazel [官方网站](http://www.noodlesoft.com/hazel.php) [本站下载](http://appwen.com/read.php?tid=137&fid=28)   
- TextExpander [官方网站](http://smilesoftware.com/TextExpander/)  [本站下载](http://appwen.com/read.php?tid=1616&fid=28)   
- Dropzone [官方网站](http://aptonic.com/)  [本站下载](http://appwen.com/read.php?tid=195&fid=28)
