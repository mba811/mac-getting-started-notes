# TextExpander

## Text Expander 的功能点

TE整个程序运行过程都在后台完成，Snippet（文本片段）可以用Group分组管理，不像iOS版那样仅支持有限的App，Mac客户端在英文输入法状态下可以在任意文本编辑器内调用，但在TE后台用户仍可以选择TE生效的程序范围：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te9.png)

### 文本替换

TE只有一个核心功能，就是文本替换，无论是频繁输入的客套话还是邮件，表情，甚至是代码模块，都可以用TE搞定，这次我们不谈理论了，枯燥得很，直接用真实案例为大家讲解：

  * 邮件

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te10.png)

我使用TE最频繁的地方就是发邮件了，经常会收到来自业务和网站读者的信件，为了提高回复效率，必须使用TE，你可以将整个邮件信息（开头，正文，落款，联系方式）加入Snippet，在调用的时候输入缩写词（Abbreviation即可）。

在这里要重点建议各位同学在设置abbr的时候要考虑到重复的情况，目前TE也已经对重复abbr的snippet进行黄色label提醒，但我们也要提前规划好，比如每一组功能不同的snippet，abbr都要不一样，这样才好区分，管理。

  * 时间定义

TE提供了丰富的时间信息格式，分Date、Time、Date/Time Math三组:

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te11.png)

Date组提供了共10种格式的年月日输入方式，可以根据使用场景灵活调用：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te12.png)

Time组提供了共9种时刻模式

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te13.png)

Snippet显示结果

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te14.png)

Date / Time Math模式挺有意思，他可以对年月日等时间单位进行加减，以此输出跳跃计时的结果，比如我要记录一个14天之后的时刻，我可以这些书写内容：

先加入一个Add Day(s)，默认输出为%@+1D，我们把D前面的1改为14；然后跟进一组普通的年/月/日格式：%@+14D%Y%B%A，输出的结果会变为：

2014八月星期六

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te15.png)

  * 指定路径

平时经常用到一些Finder路径的话可以把他们收集起来，使用TE会节省许多时间

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te16.png)

  * HTML编辑

这组Snippet是专为前端人员设计的，可以自定义各式各样的标签代码，这些Snippet都可以在窗口左下角的PreDefined Group里看到。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te17.png)

  * Markdown

使用这组Snippet可以快速插入各种Markdown固定搭配语法，比如插入图片的：

    ![](/path/to/img.jpg "Title")

或是插入H2标签：

    ## %| ##

这里要提一下#中间的“%|”，这个固定搭配的字符代表在文字输入完成之后，光标会自动回到指定位置，这种设计对于MD语法来说简直是完美的工作伙伴。后面我们还会详细说一下关于TE中光标移动的变量。

##添加Snippet的方法

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te19.png)

除了在窗口左上角点加号进入软件默认的Snippet编辑界面后，还能通过热键设定进入，如此之外你还能从以下入口添加Snippet

  * 从URL直接生成snippets group

这个功能并不是说，给一个网址，软件会自行从网页内容里随机抽取邮箱，超链，人名等信息，而是可以将远程存放在服务器的Snippet Group文件（后缀.textexpander）直接导入到Group数据库，并显示在Group列表里。

可能有朋友会问了，怎么把我自己创作的Snippet分享到网络呢？方法很简单，在TE系统内已经内置了Group导出功能，在Group列表上右键你就会发现这个选项：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te20.png)

选择“Save a Copy…”即可把Snippet Group以.textexpander为后缀保存到本地。

  * 添加TE预设好的snippets group

TE预置了9种具有代表性的Snippet组，前面我们也提到了其中一些，像Emoji，特殊字符等：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te21.png)

  * 从PopClip插件中添加

TE和Popclip的配合简直是天衣无缝，一款Popclip插件可以立即将文本拷入TE的Snippet快速设定窗口内。

### 变量扩展的魅力

Text Expander的变量扩展功能是将文本替换发扬广大的一项重要功能设计，也就是说在你应用Snippet和全文本输出之间会添加一个自定义文本变量的过程（具象的说就是一个编辑窗口），在这里，能对指定文本进行自行调整，比如赋值（single-line field），多行赋值（Multi-line field），下拉菜单（Popmenu），可选项等。

这四项变量定义功能合称：“Fill-ins”，笼统的说其他Date、Time、Date/Time Math，Key、Clipbaord，图片，光标位置调整都属于变量自定义范畴。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te23.png)

比如，你在常用业务邮件里经常会对开头的称谓进行修改，每次使用固定的Snippet可能由于疏忽会把修改的事项漏掉，别冷笑，这绝对是我们经常遇到的，而使用变量扩展则会100%避免这个问题，如下图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te24.png)

选择一段文本或一个单词，插入Single-line field，应用的时候你会看到一个弹出窗口，比如Dear后的称呼，我们改为变量扩展后，会在输入框留空，方便用户每次输入不同的称呼：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te25.png)

同理，其他变量形式也一样运用，像下图里，我们插入一个下拉菜单，每一项值（option x）可以双击进行自定义编辑。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te26.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te27.png)

使用其他的变量扩展功能能让Snippet的威力更加强大，我们可以插入图片，改变光标位置，将最近剪切板的文本插入进来，或是插入已有的Snippet内容。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te28.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te29.png)

### Snippet联想

有的时候你的Snippet数据库会有许多项目的内容性质重复，比如我有许多重要联系人的邮箱地址，那在我实际编辑邮件的任务中，如果不利用扩展变量的Popmenu的帮助我还有另一种选择：Suggestion，即Snippet联想功能。

想要使用这项功能必须满足两个条件，一个是要为这些具备同类性质的Snippets设定至少包含相同的连续2个字符的Abbr（缩写词），如下图，这样当你输入“em”这两个字符后，联想菜单才能出现；

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te30.png)

那第二个条件就是为联想菜单设定一个调用热键，我们可以在设置-Hotkeys里定义：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te31.png)

### 支持Apple Script

TE的Snippet内容模式除了纯文本和富文本，还支持Apple Script和Shell Script，TE会自动执行粘入的脚本输出成文本段落，这样的设计可以把文本替换功能发挥到机智，毕竟这种方法的自由度是最大的，比如下面这段代码：

```
set greetingsList to {"Sincerely", "Yours Truly", "Peace Out", "Have a good day", "kthxbai"}
set listLength to count greetingsList
set randomNumber to (random number from 1 to listLength)
set selectedGreeting to item randomNumber of greetingsList
return selectedGreeting
```

我可以在邮件里插入随机的不同风格的敬语，TE的预配置Group里有一个叫做：“Internet Productivity Snippets”，可以创建不同服务下的短地址，比如bit.ly、digg、is.gd等，当你copy目标url后，执行相应Snippet，就会生成专门的短地址。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te32.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te33.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te34.png)

### 数据统计，数据备份/还原等功能

TE还设计了一个数据统计模块，可显示你利用Snippets编辑文本时所节省的字符数，节省的时间（可具体到小时），还提供了图标显示。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te35.png)

TE支持通过Dropbox与其他安装 Text Expander Touch 的 iOS 设备同步 Snippets 数据，同时还设计了自动备份服务，备份频率有小时，每天，每周，每月四项可选。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te36.png)

## 参考资料

[TakeControl](http://smilesoftware.com/TextExpander/takecontrol.html)

[官方教程](http://www.smilesoftware.com/help/TextExpander/)

[Applescripting in Text Expander](http://www.smilesoftware.com/help/TextExpander/scriptingte.html)


##如何永久授权 TextExpander Helper 的控制权限

在我们介绍案例之前，我想为大家分享一下如何永久授权 TextExpander Helper 控制权限的技巧，上周就曾有朋友问过我，使用 TE 的时候总能接到以下提示：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te1.png)

每次打开 TE 都会弹出这样的提示框，让我们到「隐私-辅助功能」列表里对 TextExpander Helper 进行授权，这样 TE 才能发挥作用，可是列表里木有啊，对于这个问题，官方 Blog 就此问题给出了[解释](http://smilesoftware.com/blog/entry/yosemite-textexpander-and-accessibility-permission)，原因是 Yosemite 目前存在针对 Helper 文件的识别障碍，这种情况同样出现在了 Keyboard Maestro， Witch 等程序上。解决办法如下：

  * 打开「系统偏好设置 – 安全性与隐私 – 隐私- 辅助功能」
  * 点击窗口左下角的「金锁」按钮，在权限验证窗口输入用户名密码授权
  * 打开 「Finder – 应用程序」，找到 TextExpander，右键 -「显示包内容」
  * 在「Content – Helpers」目录下会看到 TextExpander Helper 存放在这里，将其直接托拽到应用程序隐私控制列表里
  * 重启 Mac

为以上步骤配一张图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te2.png)

还有一种方法就是利用 Cocktail 等工具对 Launch Services 数据库进行重建，但小编并不打算在这里继续详说了。

下面我们来看案例：

##  让 TE 在中文状态下使用

这个问题算是老生常谈了，但对于刚刚接触 TE 的朋友来说还是非常非常重要的，新手上来肯定会抱怨 TE 在中文输入法下切换英文半角都不能让 Snippet 生效，因为 TE 在 3.3.4 就对此功能 Cut 掉了（这其中还包括大写字母自动纠正），原因是有些用户觉得这样会与他们自定义的组合键冲突，但也有一些用户不愿意频繁切换中英文输入法来调用 Snippet，所以官方推出了一个折中的方案，设计了一个名为「TEIMPrefSetter」的设定工具（[下载](http://smilesoftware.com/downloads/TEIMPrefSetter.zip)），里面包含了官方默认排除掉的一些输入法，将他们删除就能在其输入法半角状态下应用 Snippet 了，反之，加上对应的缩写字符（比如中文就是 zh）会回到排除状态。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te3.png)

注意，操作 TEIMPrefSetter 的前后需要进行：关闭 – 打开 TextExpander 程序。

## 如何利用 TE 获取地理位置

有的时候你可能会需要在邮件中插入自己的地理位置，这种工作配合 AppleScript 也能实现，先到 Mac App Store 下载这个软件 [Location Helper for AppleScript](https://itunes.apple.com/cn/app/location-helper-for-applescript/id488536386?mt=12&uo=4&at=11lceY)，她没有独立界面，只在后台运行，当 AppleScript 脚本需要她提供用户所在地理位置，座标等数据时才在后台与脚本通信，传递数据。来看 Snippet 制作过程：

  1. 新建 AppleScript Snippet， 粘入以下脚本代码：

```
tell application "Location Helper"
    set listCoords to get location coordinates
    return (item 1 of listCoords as text) & ", " & (item 2 of listCoords) as text
end tell
```

  1. 设置 abbreviation，比如：_;gl_

  2. 测试一下，奇迹出现

## 输入带圆圈的字符

Ⓛⓔⓣⓣⓔⓡⓢ ⓘⓝ Ⓒⓘⓡⓛⓔⓢ

最近有同学在小鸟微博上将自己的username改成了以上带圆圈形式的，有些呆萌的感觉，一开始我也找不到方法，后来看 Smile 官方博客才知道这是用 TE 干的。

在 TE 上使用 「Add Group from URL…」导入一组某某人制作的现成 Snippet Group 即可，URL 输入 ：**http://smle.us/circles**， 大家可以看到导入的 Snippets，每一个圆圈字符，都用 “ooo”的前缀来定义 abbreviation，比如：

⓪ : ooo0 ① : ooo1 ⓣ : ooot

奉上我站网址logo：ⓦⓐⓔⓡⓕⓐ.ⓒⓞⓜ

## 如何与他人共享你的 Snippet？

当你创作出旷世 Snippet 后可以共享给其他好友或同事，方便其他人编辑、利用，这里的 Snippet 以 Group 为单位分享，以 Dropbox 为分发平台，操作步骤如下：

  1. 在 Dropbox 创建一个名为「Shared Snippets」的共享目录
  2. 选中待共享的 Snippet 组，点击 TE 右下角的「齿轮」图标，在下拉菜单找到一个名为「Save a Copy of Group」的选项，点击后将这个 Snippet 组保存到 Dropbox 在Mac 上的同步目录里，保存地址选择「Shared Snippets」这个共享目录，这时共享目录里的文件名为：xxx.textexpander
  3. 将 Dropbox 上保存的 Snippet 组设为「共享」，并保存生成的共享地址
  4. 回到 TE，删除原有 Snippet 组，在左下角点击「+」，选择「Add Group from File…」，将本地 Dropbox 同步目录下的 xxx.textexpander 选中。

这样，每个成员在编辑 xxx.textexpander 后都能对远程的原共享文件进行编辑，同步。

## 利用 TE 快速插入 Mail 附件

当你发邮件时有遇到过忘记加附件的情况吗？别担心，可以利用 TE 短短的一个 abbreviation 就能帮你快速打开附件选择窗口，从此不会搞错任何一封邮件，步骤如下：

– 新建一个名为「Mail Only」的 Snippet Group，生效范围，也就是 Expand in 选择 「Only These Applications…」，在应用程序列表里只选择「Mail」，这样就确保我们这个 Snippet 只作用于 Mail 里。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te4.png)

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te5.png)

– 打开OS X 自带的脚本编辑器（AppleScript），代码区粘入：

```
tell application "System Events"
    delay 0.4 -- wait a bit for snippet 'replacement' to appear
    keystroke "a" using {command down, shift down} -- key equivalent for Attach Files
end tell
```

– 保存为 .app 后缀，文件名随意起，比如：AttachFilesKeystroke.app，把这个脚本程序保存在「应用程序」目录。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te6.png)

– 在 TE 的 Mail Only Snippet Group 里，新建一个 Snippet，类型选「AppleScript」，内容插入：

```
do shell script "open -g /Applications/AttachFilesKeystroke.app/" 
return "attached"
```

– abbreviation 输入“attached”，Abbreviation type 选择 “Adapt to Case of Abbreviation” ，这样无论是 “Attached” 还是 “attached” 都能生效。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te7.png)

这样，当你在邮件正文输入 attached 时，TE 会自动运行 Snippet，弹出附件选择窗口，选择附件即可，退出窗口按 「ESC」键即可。

## 利用 TE 打造一篇万能简历

当初促使我购买 TE 的理由就是她能制作出一种万能模板，应用在求职信，常用公事往来邮件中，你不用再去逐篇修改对方称谓，非脑筋的去记各种学习经历，比如求职信，我可以用 TE 的 Snippet， 在短短的2分钟内制作出针对不同公司不同岗位的求职信，当然，这种方法只适用于撒大网找工作模式，对于目标明确的应聘公司，你还是多动脑筋，有针对性的写求职信或简历，下面我来简单介绍一下如何制作一封万能求职信的大体步骤：

**Fill-ins / Single-Line Field** 对于公司名称，对方领导称呼，我们可以在 ”亲爱的“后面插入一个 Fill-ins，「Field Name」，即填空提示，任意写，比如：公司名称/领导， 这样在填写时直接看提示填写即可，不必考虑上下文关系。在后面的「大学」，「所学专业」，「某实习单位」等需要有针对性修改的地方都可以利用 Fill-in 这个选项。

**Fill-ins/Multi-line Field** 以上 Fill-in 都是单行文本填空，其实还有多行，下拉菜单，可选内容等形式的 Fill-ins。多行填空方法和 Single-Line 一样，只是能让用户输入多行信息。

**Fill-ins/Pop Menu** 如果你学的专业并不是太冷门的，比如计算机，外语，电子商务，市场营销，那么你在找工作的过程中可选行业就比较广泛，许多公司对于一些岗位的要求不是太深，但也会需要你具备一些技能，为了赢得对方的关注，你可以量力而行，多准备一些靠谱的技能，做成 Pop Menu 的形式，在每一篇求职信里都能“对症下药”，填入对方要求或者可能感兴趣的技能，这样肯定会增加你的面试机会，比如下面这个：

**Fill-ins/Optional section** 有些求职信中，自我介绍部分，不能适用于所有用人单位，这时候你需要对这些段落进行增加或删减，无形中加大了自己的工作量，使用 Optional section /可选文本就能避免，插入 Optional section 后你只有在前面挑勾她才能出现，不勾选就会隐藏，非常方便。

整个Snippet展开后的模板样式请看这里：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/te/te8.png)

### 格式化文本

如果你需要对求职信进行精致优化，可以对 Content 选用 Formatted Text 格式，即格式化文本，可以对文本定义粗体，颜色，字号等参数，甚至可以对文本段落进行设定（居左中右），插入列表，自定义行距等等。

### 插入图片

选择格式化文本还能插入图片，你可以将个人获奖记录资料的扫描版，个人照片等资料直接插入 Snippet Content，这样在发邮件时省去了再插入图片的步骤。

## 结语

好了，我想各位如果能看到这，最起码已粗略的浏览了一篇案例介绍，是否实用，还要看你的需求，后面我们还将找机会搜集更多 TextExpander 的使用技巧和应用案例，无论你是否已入手 TE，都可以去试试上述几个应用案例，你会发现 TE 真的能帮你提高工作学习的效率，如果想入手正式版，你可以到我们的官方淘宝店「[电子薄荷](http://shop114121632.taobao.com/)」选购我们代理销售的[[中国版 TextExpander](http://item.taobao.com/item.htm?spm=a1z10.1.w4004-9376684184.9.EJcSTX&id=42450099124)]，价格为 170元，折合美元为原价（$34.95）的78折。

## 参考文章

  * [](http://smilesoftware.com/blog/entry/currency-conversion-with-textexpander)[Currency Conversion with TextExpander](http://smilesoftware.com/blog/entry/currency-conversion-with-textexpander)

  * [](http://smilesoftware.com/blog/entry/using-textexpander-to-get-location)[Using TextExpander to Get Your Location](http://smilesoftware.com/blog/entry/using-textexpander-to-get-location)

  * [](http://smilesoftware.com/blog/entry/letters-in-circles-snippet-group)[Letters in Circles Snippet Group](http://smilesoftware.com/blog/entry/letters-in-circles-snippet-group)

  * [Sharing Snippet Groups With Your Team](http://www.smilesoftware.com/help/TextExpander/sharegroups.html?_ga=1.113937031.1409188704.1418001042)

  * [](http://smilesoftware.com/blog/entry/never-forget-a-mail-attachment-using-textexpander)[Never forget a Mail attachment using TextExpander](http://smilesoftware.com/blog/entry/never-forget-a-mail-attachment-using-textexpander)