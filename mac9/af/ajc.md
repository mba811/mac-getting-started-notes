## Alfred 基础配置

### 快捷键

在 General里设置 Hotkey，我设置的快捷键是 「 +⇧+⌥+⌘+：」，这是因为我设置了 Mac 超级键并且把 「 ^+⇧+⌥+⌘+：」映射到键盘右⌘上了，别问为什么，个人习惯，我每天使用 Alfred 的频率较高，我只想把一个较为习惯的键设置为快捷键，自己摸索你也会为它找到最适合的快捷键。

![](http://lionvii.gitcafe.com/img/Alfred_set.png)

### 界面

在 Appearance 里你可以为 Alfred 找到一身合身的衣着，个人喜好，官网论坛和网络中 Alfred Themes 有各种选择。Lionvii 选了个轻盈的主题来适配 Yosemite。

![](http://lionvii.gitcafe.com/img/Alfred_theme.png)

### 基础功能

接下来我们看看没有拓展包的 Alfred 能做些什么。当用户默认快捷键「Option+SPACE」按下时，就可以在任何位置调出 Alfred 的快速搜索框，「⌘+，」或点击右上角的齿轮标识就会打开 Alfred 的设置界面。

  1.  如果搜索的关键词无法正确匹配，或者是不存在的程序或者文件的关键字，就会提示你使用搜索引擎搜索。当然,你可以可以直接指定程序来搜索，先输入搜索引擎的关键字,然后输入要搜索的内容。Alfred 还支持自定义搜索引擎:![](http://lionvii.gitcafe.com/img/Alfred_search.png)
  2. Alfred 还可以搜索文件,支持 find、open、in 三个命令。find 是搜索本地文件,open 是打开本地文件,而 in 呢,是搜索文件内的内容。搜索到文件后,点击键盘上向右键,就会打开操作界面,可以在这里选择打开文件、复制、删除、剪切、打开命令行、复制文件 路径等等操作。在 Finder 中,按下 Alfred 的 Action 默认快捷键「Cmd+Opt+\」,也会弹出这个窗口,非常便捷。
  3. 从 Alfred 中还可以直接执行控制台命令,默认设置下只有先输入,然后输入要执行的命令即可。至于直接在调出界面直接进行简单的数学运算更是不必提了。
  4. 在 Alfred 中输入 itunes,就可以打开一个 Mini 的 Player，可以方便快捷的控制音乐的播放。也可以 直接在 Alfred 中输入 play、pause、next、previous、random 来控 制 iTunes 的播放。
  5. 直接从 Alfred 中发送邮件,只要输入关键字 email ,后面加 上邮件地址并回车，程序会调用默认的邮件客户端的发送界面。 email 后面的收件人地址也可以直接从地址本都选择。
  6. 自带一个非常棒的剪贴板管理器,输入 clipboard 可以快速 调出,快捷键是「⌘+⌥+c」,有了它，ChlipMenu 等剪贴板工具都可以不要了。剪贴板工具中，还带有一个 Snippets 工具，可以方便的收集代 码片段。首先要在 Alfred 的设置页面中添加上自己需要的 snip 片段，比如设置 sj 为自己的手机号码，在任何想输入手机号码的地方，调出 Alfred 并输入「snipsj 」即可，默认的关键字是 snip，也可以根据自己的情况修改为一个更短更易于记忆的关键字。
  7. 如果你安装了 1Password，在 Alfred 中还可以直接搜索 1Password 中的密码条目，默认关键字是 1p。
  8. 执行关机、重启、锁定、打开垃圾桶、清空垃圾桶、注销、 睡眠、截图等等功能。具体命令请看下图:![](http://lionvii.gitcafe.com/img/Alfred_system.png)
  9. 调用系统的词典进行查询。输入 define 加要查询的内容就 可以自己在维基百科中搜索这个关键字。