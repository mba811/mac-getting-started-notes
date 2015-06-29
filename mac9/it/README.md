# iTerm2

iTerm2的主要特点：

  1. 开源免费。
  2. 兼容性比默认Terminal更好。对于经常要远程使用的情况下，默认的Terminal在使用vi时经常出现不兼容的问题，而iTerm2在这方面显然做的更好。
  3. 快捷键丰富。`⌘ + 数字`: 切换标签页。 `⌘ + 方向键` 按方向切换标签页。
  * `⌘ + enter`: 切换全屏
  * `⌘ + f`: 查找。支持正则。其中查找的内容会被自动复制。省去了再去⌘+c的步骤。同样，鼠标去选中的内容也会自动复制，也可以鼠标中键直接粘贴。一般在使用时，键入搜索关键词，然后用`shift-tab`或者`tab`左右自动补全，`option + enter`则自动将搜索结果键入，并且复制到剪贴板。
  * `⌘ + d`: 垂直分屏，`⌘ + shift + d`: 水平分屏。使用`⌘ + ]`和`⌘ + [`在最近使用的分屏直接切换.而`⌘ + opt + 方向键`切换到指定位置的分屏。
  * `⌘ + t` :新的标签页
  * `⌘ + w` :关闭当前标签页
  * `⌘ + ；`:自动补全历史命令。如图:自动补全

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT1.png)

  * `⌘ + shift + h`: 剪贴板历史，如图：剪贴板历史

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT2.png)

`ctrl + u`: 清空当前行。这里要注意，mac默认的ctrl+u为清楚当前光标至行首的内容，在iTerm2中则直接清除本行。iTerm2 也支持其他常用的操作命令，这里顺带讲下，因为这些命令都是mac下非常常用也很好用的：`ctrl + a`: 到行首

  1. `ctrl + e`: 行末
  2. `ctrl + f/b`: 前进后退，相当于左右方向键，但是显然比移开手按方向键更快
  3. `ctrl + p`: 上一条命令，相当于方向键上
  4. `ctrl + r`: 搜索命令历史，这个大家都应该很熟悉了
  5. `ctrl + d`: 删除当前字符
  6. `ctrl + h`: 删除之前的字符
  7. `ctrl + w`: 删除光标前的单词
  8. `ctrl + k`: 删除到文本末尾
  9. `ctrl + t`: 交换光标处文本`⌘ + —/+/0`: 调整字体大小
  * `⌘ + r`:清屏，其实是滚到新的一屏，并没有清空。ctrl + l 也可以做到。
  * 更多实用功能：Exposé 标签 按`⌘ + opt + e `打开Exposé，并支持搜索。如图：Exposé

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT3.png)

  * 全局呼出快捷键。如图： 呼出快捷键

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT4.png)

  * `⌘ + /`: 找到当前光标位置，有时会很有用。
  * `shift + ⌘ + s`: 保存当前窗口快照。
  * `⌘ + opt + b`: 快照回放。很有意思的功能，你可以对你的操作根据时间轴进行回放。可以拖动下方的时间轴，也可以按左右方向键。如图：快照回放

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT5.png)

  * 支持256色。方便配置vi配色。但是在某些远超服务器上不支持256色，则只要在Prefences->Profiles->Terminal里设置为xterm。

# zsh

zsh作为bash的替代品，自然很多人要问：why zsh？ 在[Zsh Workshop](http://www.acm.uiuc.edu/workshops/zsh/why.html) 有个长长的功能列表，用来回答这个问题。这里讲下我选择zsh的原因，当然，也是介绍zsh强大的功能。

  1. 兼容bash。这使得切换到zsh没有任何成本。
  2. OS X默认的bash版本实在是太老了啊……
  3. 拼写纠正。你总会不小心打错命令。这时，zsh会进行自动拼写纠正，如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT6.png)

更强大的补全。

  * 连按两次tab会列出所有的补全列表并直接开始选择。如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT7.png)

  * 并且可以用方向键来选择，但是对我这种很少用方向键的人来说只能猛敲tab了么，不是，zsh支持使用`<ctrl-n/p/f/b>`来选择，perfect!
  * 命令选项补全。有多少人依然记不住tar的命令选项？中枪的去抄20遍……在zsh中只需要键入`tar - <tab>`就会列出所有的选项和帮助说明。用了zsh之后`man`少用了好多……
  * 命令参数补全。zsh 对命令的参数补全也很强大。键入`kill <tab>`就会列出所有的进程名和对应的进程号。如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT8.png)

这还不够，试试键入`kill sbin <tab>`,如图所示:

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT9.png)

  1.     * 自动为sbin这个进程名补全了进程号。kill进程再也不用两步操作了。
  2. 更智能的历史命令。在用`<ctrl-p>`或者`方向上键`查找历史命令时，zsh支持限制查找。比如，输入`ls `然后再按方向上键,则只会查找用过的ls命令。而此时使用`<ctrl-p>`则会仍然按之前的方式查找，忽略`ls`。
  3. 多个终端会话共享历史记录。经常有多个窗口，tab，tmux的多个session，panel。这些命令历史不能共享实在是很糟糕的回忆。但是有了zsh之后，这些确实成了回忆了,所有的命令历史都可以共享。
  4. 更智能的`cd`。首先你甚至不需要再输入cd了，直接输入路径即可。第二，在你知道路径的情况下，比如`/usr/local/bin`你可以输入`cd /u/l/b`然后按`<Tab>`进行补全快速输入。这显然不够，zsh还支持路径替换，如果你其实想进入的是`/usr/local/bin`，不再需要`../` 了，直接在当前输入`cd bin share`即可，则`bin`会替换为`share`。在之后我会介绍z和autojumper，目录跳转会更方便。
  5. 更强大的alias。zsh不仅支持普通的alias，例如：`alias ls ='ls --color=auto'`。zsh还支持后缀alias,即以什么命令打开特定的后缀名文件。例如`alias -s js=mvim`,输入`hello.js`，会以vim打开该文件,而不在需要`vim hello.js`。
  6. 通配符搜索。这也是我最爱的功能之一。之前讲过由于命令补全少用了很多`man`命令，而这个功能让我少用了很多`find`命令。 一般的通配符搜索无非是`ls -l *.log`,如图:

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT10.png)

在zsh中可以做到递归的通配符搜索。使用`**/`来递归搜索，如图

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT11.png)

  1. 是不是在很多场景下可以取代`find`？

以上都是我感觉迁移到zsh之后非常实用的功能。要想从头开始了解和学习zsh，可以访问[A User’s Guide to the Z-Shell](http://zsh.sourceforge.net/Guide/zshguide.html)。不过大家都很忙，从头开始自己学习和配置会很累。所以现在说到zsh，不得不提的就是[oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh?source=c),oh-my-zsh是一个开源的zsh配置管理框架，提供了大量实用的功能，主题等。现在基本都是标配了吧。如图是我在用的默认zsh主题`robbyrussell`，如图

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT12.png)

可以发它能自动显示当前所在的git分支以及当前本地状态（黄色的小叉表示本地有更新未提交）。

当然zsh也不是完美无缺。在我使用过程中有两点不是很舒服： 1. 自动纠正并不总是那么智能。如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT13.png)

但是可以对这些命令使用alias 加上`nocorrect`前缀，如：

`alias rake deploy='nocorrect rake deploy'`

  1. 一些符号是zsh中保留的，使用需要转义，如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT14.png)

下面讲下zsh和oh-my-zsh的安装。

**使用brew来安装zsh**

`brew install zsh`

**设置zsh为默认**

在`/etc/shells`文件末尾添加

`/usr/local/bin/zsh`

执行：

`chsh -s /usr/local/bin/zsh`

最后记得将`~/.bash_prorile`或者`~/.profile`等配置拷贝到~/.zshrc中。

**安装oh-my-zsh**

自动安装:

    curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh

可以选择自己喜欢的[主题](https://github.com/robbyrussell/oh-my-zsh/wiki/themes)。只需要修改`~/.zshrc`文件中的`ZSH_THEME`即可。

# z和autojump

[z](https://github.com/rupa/z)和[autojump](https://github.com/joelthelion/autojump)的功能类似，前者是简单的shell脚本实现，后者由python实现，功能都是可以方便自动匹配到你最多使用的目录并跳转。我在用的是z，如图

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/iTerm2/iT15.png)

，我在根目录输入`z github`可以自动跳转到我常用的`notice501.github.com`这个目录，也就是本博客的工程目录。超级方便的工具。autojump用法类似，命令为`j`而不是`z`两者的安装方式：

**z**
    
    git clone git@github.com:rupa/z.git

而后将z.sh放入环境变量即可。

**autojump**

autojump可以直接使用brew安装
    
    brew install autojump



## iTerm2 与 zsh + tmux 配合使用的一些心得

## tmux是什么

[tmux](http://tmux.sourceforge.net/) 是什么？我们先来看看官网的解释：

tmux is a terminal multiplexer

What is a terminal multiplexer? It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal. And do a lot more.

简单来说就是一个终端多开工具，能让你同时运行多个终端会话，在这些会话之间随意切换。

## 特色功能

## 终端会话多开

平常在终端的使用过程中，一次只能运行一个会话。 当然你也可以通过终端程序的多开标签页来解决，但是使用了tmux，你就可以在一个终端中同时运行多个会话，只需开启一个终端。[![终端会话多开](http://lszb811.qiniudn.com/tmux1.png)](http://lszb811.qiniudn.com/tmux1.png)终端会话多开

## 会话的分离（detach）与连接（attach）

我们在使用终端的过程中，总会遇到过类似场景：

  * 用终端运行了一个测试代码的HTTP服务（如rails、django），想要关闭终端程序窗口，但又不想让服务停掉
  * 用ssh连接到服务器，正在编辑文件或修改配置，突然断网了，网络重新连通后再连接上服务器，又要重新进入刚才的工作目录、找到要编辑的文件、找到刚才修改的那一行……
  * 在公司用ssh连接到服务器，打开了多个文件，回家后想继续干活，但是还要再凭记忆把文件逐一打开

使用tmux会话的分离与连接就可以轻松解决以上问题，分离（detach）可以使终端会话在后台运行，连接（attach）可以重新打开在后台运行的会话，也可以多个终端连接同一会话。这些都会在后续详细描述。

tmux是什么 [http://t.cn/Rv6DnPb](http://t.cn/Rv6DnPb) 平常在终端的使用过程中，一次只能运行一个会话。 当然你也可以通过终端程序的多开标签页来解决，但是使用了tmux，你就可以在一个终端中同时运行多个会话，只需开启一个终端。

## 安装

tmux 的安装比较简单，以下分别介绍 linux、Mac、FreeBSD、Windows系统下的安装方法

## linux

linux 用户只要使用系统自带的包管理器来安装就行了

### Debian 系
    
    $ sudo apt-get install tmux
    

### 红帽系
    
    $ sudo yum install tmux
    

### Arch Linux
    
    $ pacman -S tmux
    

## Mac

Mac 用户可以通过 [Homebrew](http://brew.sh/) 或 [Macports](http://www.macports.org/) 来进行安装

### Homebrew
    
    $ brew install tmux
    

### Macports
    
    $ sudo port install tmux
    

## FreeBSD

FreeBSD可以使用自带的port进行安装
    
    $ cd /usr/ports/sysutil/tmux
    $ make install clean
    

## Windows

Windows下可以使用 [cygwin](http://cygwin.com/) 来安装 cygwin，cygwin是图形安装界面，请确保在 Select Packages 界面出现时，选中 tmux 即可。

最后，为了确保 tmux 正确安装，可以在命令行里输入以下命令，来查看 tmux 的版本号
    
    $ tmux -V
    

_注意是大写的V_

如果出现类似以下字符串，就已经安装成功了
    
    tmux 1.8
    

目前最新版本为 1.9a，随后的章节将使用 1.8 版本做解说，请确保你安装的 tmux 版本要在 1.8 或以上，以免缺少某些必要的功能。

## 会话

上一节我们已经将 tmux 安装好了，现在就可以通过以下命令来启动它：
    
    $ tmux
    

启动之后，可以看到命令行最底部多了一条绿色的状态条，上面显示了一些信息，比如计算机名和时间等。 要退出 tmux，可以输入`exit` 回车或者按下组合键 `[Ctrl+d]` 。

其实刚才我们启动 tmux 之后，它已经自动创建了一个会话（Session），会话是 tmux 的最主要的功能，接下来我们将介绍会话的一些功能。

## 新建会话

启动 tmux 会自动创建会话，但并没有为会话命名。为了以后使用方便，我们来创建一个自己命名的会话，命令如下：
    
    $ tmux new-session -s <会话名称>
    

现在我们来创建一个会话，取名为 `dev` ，命令为：
    
    $ tmux new-session -s dev
    

创建完成之后，可以看到底部状态条左边标示出了当前的会话名为 `dev` 。

这个命令还有一个缩写版本， `new-session` 缩写成 `new` ，也就是上述命令可以简写成：
    
    $ tmux new -s dev
    

新建会话还可以带上一个初始命令：
    
    $ tmux new -s <会话名称> 初始命令
    

比如创建一个名为 **monitor** 的会话，初始命令为 **top** ：
    
    $ tmux new -s monitor top
    

可以看到会话创建后，会自动运行 **top** 命令。但是一旦退出 **top** 程序 (按 `[q]` )，会话也会自动退出，所以在实际应用中，初始命令几乎不会用到。

## 分离会话（detach）

之前已经说过，退出 tmux 可以使用 `exit` 命令或者 `[Ctrl+d]` 组合键，退出 tmux 会把会话结束掉，就像平常关闭终端程序一样。但是在实际应用中，可能你并不希望这样，因为有些程序是要保持运行的，例如 rails 的测试服务、telnet连接远程服务器等等。

这时候分离会话就可以派上用场了，分离后的会话并不会把运行中的程序结束掉，而是会保持运行，你还可以稍后重新连接上这些会话。

分离会话之前，我们先来启动一个需要保持运行的程序，这里用 python 2.x 的 SimpleHTTPServer 为例， 当然你也可以选择启动 rails 或 django 的测试服务、telnet 连接或者更简单的 top 命令。

先在之前创建的会话中运行一下命令来启动一个简单的 HTTP 服务：
    
    $ python -m SimpleHTTPServer
    Serving HTTP on 0.0.0.0 port 8000 ...
    

这时候 HTTP 服务已经运行起来了，接下来就要做分离会话的操作了，快捷键是：

`[Ctrl+b]` `[d]`

也就是先按下组合键 `[Ctrl+b]` 然后再接着按 `[d]` 。d 代表了 detach，而 `[Ctrl+b]` 是一个命令前缀（官方称之为 prefix），这个命令前缀是告诉终端程序，接下来的命令是针对 tmux 使用的。在之后的描述中，都将采用 `[前缀]` 来代替 tmux 的命令前缀。

可以看到，在按下快捷键之后，tmux 已经退出并回到平常的终端中，并带着 **[detached]** 字样的提示。

这时候可以在浏览器访问一下刚才启动的 HTTP 服务 [http://localhost:8000，确实可以正常访问，证明刚才的程序还在保持运行中，并没有被结束，甚至你还可以把整个终端程序关闭。](http://localhost:8000%EF%BC%8C%E7%A1%AE%E5%AE%9E%E5%8F%AF%E4%BB%A5%E6%AD%A3%E5%B8%B8%E8%AE%BF%E9%97%AE%EF%BC%8C%E8%AF%81%E6%98%8E%E5%88%9A%E6%89%8D%E7%9A%84%E7%A8%8B%E5%BA%8F%E8%BF%98%E5%9C%A8%E4%BF%9D%E6%8C%81%E8%BF%90%E8%A1%8C%E4%B8%AD%EF%BC%8C%E5%B9%B6%E6%B2%A1%E6%9C%89%E8%A2%AB%E7%BB%93%E6%9D%9F%EF%BC%8C%E7%94%9A%E8%87%B3%E4%BD%A0%E8%BF%98%E5%8F%AF%E4%BB%A5%E6%8A%8A%E6%95%B4%E4%B8%AA%E7%BB%88%E7%AB%AF%E7%A8%8B%E5%BA%8F%E5%85%B3%E9%97%AD%E3%80%82/)

_可能有人会很不习惯这个默认的命令前缀，包括我自己在内，因为 `[Ctrl+b]` 是一个 Emacs 或 Vim 的快捷键，甚至是命令行本身的快捷键。在 Emacs 或者命令行中，它是后退一个字符的操作；而在 Vim 中，它是一个向上翻页的操作。不过不用担心，先忍耐忍耐，稍后的章节将讲述如何配置 tmux，那时就可以摆脱快捷键冲突的困扰了。_

## 连接会话（attach）

被分离的会话，还可以重新连接上，就让我们来实践一下，命令为：
    
    $ tmux attach-session -t <目标会话名>
    

简写为
    
    $ tmux attach -t <目标会话名>
    

或
    
    $ tmux a -t <目标会话名>
    

之前我们创建的会话名叫 **dev** ，所以命令就可以这样写：
    
    $ tmux a -t dev
    

因为我们只创建了一个会话，所以可以忽略 **-t** 的参数，直接写成：
    
    $ tmux a
    

如果不指定目标会话名，tmux 将会连接你上次使用的会话。连接上 **dev** 会话之后，可以看到程序还在运行中，而且终端里显示的内容跟会话分离前没什么两样，只是多了几行 HTTP 请求的日志。

这时候，你还可以在多个终端，甚至是多台电脑通过 ssh 连接上同一个会话，可以实现共同操作，非常强大，具体的感受可以自己体会。

接下来我们多创建几个 tmux 会话，在这之前先把当前会话分离掉：

  1. 分离当前会话： `[前缀]` `d`
  2. 新建一个名为 **edit** 的会话： `$ tmux new -s edit`
  3. 分离 **edit** 会话： `[前缀]` `d`
  4. 新建一个名为 **telnet** 的会话： `$ tmux new -s telnet`
  5. 分离 **telnet** 会话： `[前缀]` `d`

现在，会话已经足够多了，接下来登场的就是列出所有会话的命令：
    
    $ tmux list-sessions
    

可以简写成
    
    $ tmux ls
    

屏幕上将会显示出所有创建的会话，比如：
    
    dev: 1 windows (created Tue Jun 10 15:10:32 2014) [80x24]
    edit: 1 windows (created Tue Jun 10 16:26:20 2014) [80x24]
    telnet: 1 windows (created Tue Jun 10 16:26:53 2014) [80x24]
    

这时候连接会话的 **-t** 参数就派上用场了，你可以选择连接到哪一个会话。

如果没有创建会话或者会话都全已退出，那么列出所有会话的命令将会提示一个 **failed to connect to server** 的信息，可以看得出来 tmux 是有运行一个服务的，这个服务管理着所有的会话，并让他们持续运行。

### 小结

通过创建多会话，以及分离/连接的功能，还能实现多终端连接同一会话，已经完全可以轻松应付许多平常很以实现的功能。在下一章节中，我们将讨论 tmux 里窗口（Window）的功能。

## 窗口

上一章节介绍了 tmux 的会话，接下来就要讲到 tmux 中窗口的使用。

其实当你新建一个会话的时候，tmux 已经自动给你在新会话中自动创建了一个窗口(Window)，窗口的编号从0开始，名称则默认为 **当前工作目录** 或者 **当前运行的程序** ，都显示在下方的状态条中。如下图所示，我将工作目录切换到了 `~/Documents` ，窗口0的名称也随之变换。

[![默认窗口名](http://lszb811.qiniudn.com/tmux2.png)](http://lszb811.qiniudn.com/tmux2.png)默认窗口名

我们也可以在创建会话的时候附上 `-n` 参数，来给窗口制定一个名称
    
    $ tmux new -n <窗口名>
    

`-n` 参数可以和之前介绍过的 `-s` 参数一同使用，现在我们来创建一个名为 **demo**的新会话，新建窗口取名为 **worldcup** 吧。
    
    $ tmux new -s demo -n worldcup
    

_[注意] 装了 oh-my-zsh 的话，自定义窗口名不起作用，无论如何设置或更改窗口名，敲入命令之后窗口名都会变成当前工作目录或者当前运行的程序，希望新版本能修复这个问题_

## 新建窗口

新建窗口比较简单，只要执行以下组合键即可。

`[前缀]` `c`

**c** 代表了 **create** ，一个会话可以创建多个窗口，但是为了窗口之间切换的方便，建议将窗口个数保持在个位数。

## 切换窗口

切换窗口有好几种方式，我们先来说说最常用的两种。

上一个窗口（previous）： `[前缀]` `p` 下一个窗口（next）： `[前缀]` `n`

使用这两种方式，就可以在所有窗口中按顺序切换。如果在第一个窗口执行上一个窗口的操作，则会跳转到最后一个窗口，同样的在最后一个窗口执行下一个窗口的操作，则会跳到第一个。

当然每个窗口都有一个编号，你也可以通过以下简单的操作，来跳转到制定编号的窗口。

跳转到指定窗口： `[前缀]` `0-9的数字`

由于这个指令只能在 0-9 号的窗口之间跳转，所以建议窗口个数保持在个位数。

但是如果窗口个数实在太多，还可以用以下方法来呼出窗口列表，用上下键就可以进行选择，然后回车。

窗口列表： `[前缀]` `w`

[![窗口列表](http://lszb811.qiniudn.com/tmux3.png)](http://lszb811.qiniudn.com/tmux3.png)窗口列表

## 更改窗口名称

更改窗口名称也比较简单，首先要先切换到需要修改的窗口下，执行以下操作，就可以进行修改了。

更改窗口名称： `[前缀]` `,`

这时，底部的状态条会变成黄色，只要输入想要取的名字，回车即可。

[![更改窗口名称](http://lszb811.qiniudn.com/tmux4.png)](http://lszb811.qiniudn.com/tmux4.png)更改窗口名称

## 关闭窗口

当窗口不再需要时，也可以进行关闭，以下是操作指令。

关闭窗口： `[前缀]` `&`

这个命令确实不太好用，还要用到 `Shift` 键，但是别着急，讲到自定义配置的时候，就可以对默认的组合键进行更改了。关闭窗口之前，状态条也会有黄色的确认提示，输入 `y` 确认或者 `n` 取消。

[![关闭窗口](http://lszb811.qiniudn.com/tmux5.png)](http://lszb811.qiniudn.com/tmux5.png)关闭窗口

当会话中所有的窗口都关闭之后，会话也会随着退出。

### 小结

本章讲述了 tmux 中如何使用窗口，窗口是会话的子元素，当然窗口还能再分，也就是下一章讲述的面板。

## 窗格

上一章已经介绍了 tmux 里的窗口，窗口也可以再分，也就是接下来要说的窗格（pane）。我们已经知道，tmux 下可以有多个会话，会话下又可以有多个窗口，那么同样，窗口下还可以有多个窗格，其结构如下。
    
    tmux
    ├── 会话a
    │   ├── 窗口a
    │   │   ├── 窗格a
    │   │   └── 窗格b
    │   └── 窗口b
    │       └── 窗格c
    └── 会话b
        ├── 窗口c
        │   └── 窗格d
        └── 窗口d
            └── 窗格e
    

## 切分窗格

一个窗口可以切分成多个窗格，主要的切分方法有两种，垂直切分和水平切分。

垂直切分（把窗口垂直切分成左右两等分）： `[前缀]` `%`[![垂直切分](http://lszb811.qiniudn.com/tmux6.png)](http://lszb811.qiniudn.com/tmux6.png)垂直切分

水平切分（把窗口水平切分成上下两等分）： `[前缀]` `"`[![水平切分](http://lszb811.qiniudn.com/tmux7.png)](http://lszb811.qiniudn.com/tmux7.png)水平切分

以上两种切分方法还可以混合使用，比如先进行水平切分再进行垂直切分，我们会得到类似以下的3个窗格。

[![水平切分+垂直切分](http://lszb811.qiniudn.com/tmux8.png)](http://lszb811.qiniudn.com/tmux8.png)水平切分+垂直切分

## 切换工作窗格

把窗口切分成多个窗格以后，就需要在各个窗格直接进行切换，以便对不同的窗格进行不同的操作。

窗格切换： `[前缀]` `o`

这个指令会在当前窗口的所有窗格中轮流切换，如果窗格比较少的情况下，非常实用。但是如果窗格太多，就比较麻烦了，可以用以下指令来制定切换的方向，自己体会一下吧。

按制定方向切换窗格： `[前缀]` `方向键`

## 更改窗格布局

tmux 有五个默认的窗格布局，可以满足基本的工作需要。

  1. 水平平分（even-horizontal）
  2. 垂直平分（even-vertical）
  3. 主窗格最大化，其他窗格水平平分（main-horizontal）
  4. 主窗格最大化，其他窗格垂直平分（main-vertical）
  5. 平铺，窗格均等分（tiled）

以下操作指令，可以在这五个默认的窗格布局之中轮流切换。

更换窗格布局： `[前缀]` `空格`

## 小结

到本章为止，tmux 最基本的操作已经讲述完，在接下来的章节中，要给大家介绍一下 tmux 的命令（command）
