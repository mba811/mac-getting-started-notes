最近学习苹果认证的《Mac OS X Support Essentials》教程，看到 Command Line 一节有很多实用的知识，下面选取一部分翻译 + 笔记，整理成此文。

> 你可以整天驾驶汽车而不用知道如何修理它们，但是如果你希望当一个维护员，你就需要知道事情是如何运作的。同样的事情也发生在了 Mac OS X 上；你可以一直使用 Mac 而不用知道如何修理它，但是如果你想对系统做一些维护或解决一些问题，那么你需要知道如何使用 command-line。

## 为什么要使用命令行/如何开启命令行？

  * 许多功能在图形界面不提供，只有通过命令行来实现。
  * Finder会隐藏许多你不太会需要的文件，然而 command line 会允许你访问所有文件。
  * 通过 command line 可以远程访问你的 Mac（利用 SSH）。
  * administrators 用户可以通过 `sudo` 命令获得 root 用户权限。
  * 通过 command-line script 可以使工作更高效。
  * Terminal（终端）程序可以在“实用工具”里找到。
  * 如果你开启手动输入用户名登陆模式，登陆时在用户名处输入 `>console` 可以直接进入命令行界面。随后你仍然需要登录到一个账户。

## 初识Command Line

  * 许多命令会花费一些时间来执行，然而这中间不会给出任何提示或者进度条。一般结束后会出现一个“用户名$”的标记。如果没有出现，那么说明最后一条命令正在执行。
  * 一条命令包括 Command Name、Options、Arguments、Extras 四个部分，但是后三个部分有时是可选的。Options 部分用`-`作为前导符。其中许多命令的 Options 部分只包含单个字母，这时可以合并。例如，`ls -lA`和`ls -l -A`是等效的。Arguments 部分用来细化这个命令或指定这个命令具体的实施对象，Extras 部分则用来进一步实现其他功能。
  * 举例：下列命令包含前三个部分，用于删除 Junk 这个程序。

`michelle$ rm -R /Applications/Junk.app`

  * 如果你输入了一些错误的命令，系统会返回一些错误信息。但是系统却不会阻止你做傻事（例如删除整个用户文件夹）。

## 关于 man 命令

虽然有上千条命令，每条命令还有许多可选参数和具体的使用方式，但是你却不需要记住这些命令。你只需要记住一个：`man`

大多数命令都会包含一个使用指南，会告诉你任何你需要知道的关于这个命令的所有细节，在命令行中输入 `man command-name` 即可获取。例如，你想知道`ls`这个命令怎么使用，输入`man ls`即可进入使用指南页面。

使用指南往往很长，所以你可以使用▲（上箭头）或▼（下箭头）来上下移动，使用　来翻页，输入`/`和关键字来按照关键字搜索，按Q来退出使用指南页面。

那么——如果你连命令名称都不知道怎么办呢？输入`man -k`和关键字来对整个使用指南数据库进行搜索。

## 命令行，文件和路径

> 如果知道如何使用命令是掌握 command line 的第一步，那么第二步就是学习如何在 command line 中使用文件路径。如果你掌握了文件路径，你将会发现这比使用 Finder 更加快捷。

**注意**

  * command line 工具是大小写敏感的，并且对于文件名，必须包括扩展名。例如，你想找iTunes这个程序，输入`itunes`是无效的，必须输入`iTunes.app`。
  * Mac OS传统上喜欢使用“文件夹”（folders）这个名称，但是在 command line 中，主要使用“目录”（directory）这个词。这和 UNIX 是一致的。

### 两种路径：绝对路径和相对路径

  * 绝对路径：完整描述一个文件的位置，总是以斜杠（`/`）（forward slash）开头。例如`/Users/michelle/Public/Drop Box`。
  * 相对路径：只描述一部分位置信息，它和你在 command line 目前的目录有关。当你打开新的 Terminal 程序时，command line 会话的目录应该是你的 home folder。这时上面例子文件夹的相对路径写作`Public/Drop Box`。显然它从当前目录开始。和html类似，你也可以使用两个点（“`..`”）来代表父目录，这样你就可以用相对路径表示上级或同级目录了。例如你可以输入`cd ..`甚至`cd ../..`

### 切换到其他路径和目录

如果你想将当前 command line 会话切换到其他目录，需要用到三个命令：`pwd`，`ls`和`cd`。

  1. `pwd`的含义是“print working directory”，会显示当前目录的绝对路径。
  2. `ls`的含义是“list directory contents”，它会列出当前目录的内容。这个命令还有其他参数可选。
  3. `cd`的含义是“change directory”，它会改变当前目录到你指定的目录。如果你不指定，则会返回你的 home folder。

### 处理特殊字符

如果目录中有特殊字符（空格，括号，引号，`[]`，`!`，`$`，`&`，`*`，`;`，`|`，`\`），那么直接输入空格会造成系统识别困难，必须使用特殊的语法来表示这些字符。例如上例中，空格前添加反斜杠“`\`”（back slash）即可：`cd Punlic/Drop\ Box/`。除了反斜杠，也可以用引号的方法：`cd "Public/Drop Box"。`

——如果不想手动输入，也可以把文件从 Finder 拖到 Terminal 窗口来创建绝对路径，这会方便一些，因为上面提到的所有特殊字符在拖动后都会自动变成系统可识别的表示方法。其实，更有效率的解决方案是使用 Tab Complete 功能。

Tab Complete 是 command line 中最能给你节省时间的特性之一，利用它的自动完成文件、目录名称功能还可以防止你输入错误。使用`cd`进入你的 home folder，使用`cd P`命令，然后按下tab按键。你可能会听到错误音，因为你的 home folder 内有多个 P 开头的文件夹。再按一次tab，Terminal 将会为你列出 P 开头的两个文件夹：Public 和 Pictures。按U，再按tab，Terminal 则会自动为你补全`Public/`。Tab complete 同样会处理那些特殊字符。注意，这会在末尾保留`/`符号，大部分时候这没问题，但如果出错，移除多余的`/`试一试。

另外，鄂化符`~`（tilde）在command line 中可以代表当前用户的 home folder。例如`~/Public/Drop\ Box/`是合法的。

### 查看隐藏文件

为了简化工作，command line 和 Finder 都会隐藏许多文件和文件夹，这些内容通常是系统需要的。不借助第三方工具让 Finder 显示隐藏文件比较困难，但是在 command line 中却非常简单。首先，许多隐藏文件的隐藏是通过隐藏属性在 Finder 中隐藏的，而 command line 会忽略这些属性，所以这些文件会在 command line 中显示。另外，`ls`命令会隐藏文件名以`.`开头的文件，但是这些文件却可以被显示出来，方法是利用`-a`选项。例如：
    
    michelle$ ls -la
    

我们还添加了`-l`选项，目的是控制输出格式。如果你注意输出内容的话，会发现还包括`.`和`..`两项，它们分别表示当前文件夹和父文件夹（如图）。如果你不想显示这两项，只需要把`-a`改成`-A`即可。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m8-1.png)

### 前往其他卷

在 command line 中，系统卷（也称为 root volume）是由开始的一个正斜杠表示的。然而也许听起来不可思议，在 command line 中其他卷看起来就在文件系统中一个叫做 Volumes 的文件夹中。下面的命令清晰地显示出这种逻辑关系：我从我的 home folder 出发，最终前往一个叫 Time Machine 的卷，该卷是外接在 Mac 上的。
    
    bogon:~ renfei$ pwd
    /Users/renfei
    bogon:~ renfei$ cd /Volumes/
    bogon:Volumes renfei$ pwd
    /Volumes
    bogon:Volumes renfei$ ls
    Macintosh SSD &nbsp; &nbsp; &nbsp;Time Machine
    bogon:Volumes renfei$ cd Time\ Machine/
    bogon:Time Machine renfei$ pwd
    /Volumes/Time Machine
    

## 用Command-Line管理文件

### 检视文件

有许多基础命令用来定位、检视文件和文件夹，包括`cat`, `less`, `which`, `file`以及`find`。别忘了，你可以利用`man`命令来查阅每个命令的使用指南。

#### cat

`cat`是“concatenate”的意思，会按顺序读取文件并输出到 Terminal 窗口，语法为`cat`后接你需要查看的文件的路径。`cat`命令也可以用`>>`来增加文本文件的内容，例如命令`cat ../textOne.txt >> textTwo.txt`会把 textOne.txt 的内容添加到 textTwo.txt 的结尾。这个`>>`就属于上一篇提到的“Extras”。

#### less

这个命令更适合用来查看长文本文件，因为它会允许你查找文本。语法为 `less`后接文件路径，和`cat`一样。用`less`命令打开的文件其实和你查看命令使用指南的时候使用的是一个查看器，所以操作是相同的，同样可以使用▲（上箭头）或▼（下箭头）来上下移动文本，使用　来翻页，输入`/`和关键字来按照关键字搜索，按Q来退出使用指南页面。除此之外，按V键来使用`vi`文本编辑器。

#### which

这个命令会定位某个命令的文件路径。换言之，它会告诉你你执行某个具体命令的时候，在使用哪个文件。语法为`which`后接某个命令。如图：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m8-2.png)

#### file

这个命令会尝试根据文件的内容输出文件类型。如果一个文件缺失了扩展名，那么这个命令可能会非常有用。语法为`file`后接文件路径。如图，此例为一个 PNG 文件，还给出了它的尺寸、颜色数等信息。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m8-3.png)

#### find

这个命令用来根据搜索关键词定位文件路径。 `find`命令不使用 Spotlight 搜索服务，但是它允许你设置非常具体的搜索条件，以及通配符（稍后介绍）。语法为`find`后接搜索的起始路径，后接定义搜索的选项，后接搜索内容（包含在引号里）。例如：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m8-4.png)

**注意**

  1. 如果你要搜索根目录，也许你想使用`-x`选项来避免搜索 /Volumes 文件夹。
  2. 如果想使用 Soptlight 搜索服务，使用`mdfind`命令后接搜索关键词即可。

### 使用通配符（Wildcard Characters）

下面是常用的通配符：

  * 星号（＊，Asterisk）——代表任何长度的任何字符。例如`*.tiff`代表所有格式为tiff的文件。
  * 问号（?，Question mark）——代表任何单个字符。例如`b?ok`匹配 book 但是不匹配 brook。
  * 方括号（[]，Square brackets）——定义一定范围的字符，例如`[Dd]ocument`匹配 Document 以及 document；`doc[1-9]`匹配doc1, doc2, …, doc9。

配合使用上面三种通配符可以大大提高效率。

### 使用递归命令

简单来说，递归命令可以允许命令不执行于一个特定文件，而是指定的路径下的所有文件。大多数命令包含一个`-r`或者`-R`选项，来设定你想递归地执行这个命令。例如下面的例子，展示了添加`-R`后`ls`命令的执行方式：

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/mac/m8-5.png)

### 编辑文件和文件夹

有许多基础的命令用来编辑文件和文件夹，包括`mkdir`, `cp`, `mv`, `rm`, `rmdir`以及`vi`。下面我们来简要地介绍一下这些命令。

#### mkdir

“make diretory”的缩写，用来创建文件夹，语法为`mkdir`后接新文件夹的目录。可以用`-p`选项，来一起创建路径中不存在的文件夹（这样你就不用挨层创建了）。

#### cp

“copy”的缩写，用来把文件从一处复制到另一处。语法为`cp`后接原始路径，后接目标路径。如果你想复制整个文件夹和所有内容，需要添加`-R`选项。如果指定的目标路径不含文件名，则 cp 命令会按原名复制。如果指定的目标路径包括文件名，则会复制为你指定的文件名。如果仅指定新文件名，则会在原处以新名称创建文件副本。注意，系统会自动替换同名文件而不出现提示。

#### mv

“move”的缩写，用来移动文件。语法为`mv`后接原路径，后接新路径。mv 的指定路径规则和 cp 是一样的（没错，如果仅指定新文件名，它就成了重命名命令）。

#### rm

“remove”的缩写，会永久删除文件。注意，command-line中没有废纸篓。语法为`rm`后接文件路径。然而，使用 rm 命令删除的文件有可能可以通过数据恢复工具恢复。如果希望安全删除文件，可以使用`srm`命令。

#### rmdir和rm -R

rmdir是“remove directory”的缩写，这个命令会永久删除文件夹。再强调一遍，CLI 中木有废纸篓。语法为`rmdir`后接希望删除目录的路径。然而，rmdir 命令无法删除含有任何其他文件的文件夹，所以大多数情形下`rmdir`命令是不适用的。不过，你可以利用`rm`添加`-R`选项来删除文件夹及包含的所有文件。

#### vi

代表“visual”（视觉的），然而这个名称相当具有讽刺意味：vi可能是可视化效果最差的文本编辑器了。然而，vi 是 command line 中最常见的文本编辑器。用vi打开文本文件，只需要输入`vi`后接文件路径即可。Mac OS X 还提供了`nano`，一个更加现代的文本编辑器。它也更加方便，例如在底部包含了一个作弊小条（=_=），上面有常用的快捷键列表（你就不用背下来它们了）。然而，vi却有时是默认的文本编辑器，所以掌握vi是很有用的。

和`less`命令类似，`vi`命令会占用整个 Terminal 空间来显示文件内容。打开后，在“command模式”，vi 会等你输入一些预定义字符来告诉 vi 你想做什么。你也可以使用键盘上的箭头键单纯地浏览文件。你想编辑时，按A开始（会进入编辑模式）。文字会插入到光标处。如果你想保存，需要先退出编辑模式进入 command 模式。方法是按下esc键。回到 command 模式后，按住shift同时按两次Z来保存并退出。如果你不想保存，在 command 模式输入`:quit!`并按enter  
return直接退出。

## 用Command-Line管理系统

### 使用su来切换用户

`su`命令代表“substitute user identity”，允许你在命令行中轻松切换到另一个用户账户。语法为`su`后接用户的短名称。然后会要求你输入密码（但是输入的时候不会显示）。执行完毕后，命令的前缀会改变，表示你拥有其他用户的权利。你可以利用`who -m`命令来验证当前登陆的身份。切换后，你会一直保持该用户身份，直至退出 Terminal 或者输入`exit`命令。

### 关于sudo的使用

#### sudo概述

更强大的命令就是`sudo`，代表“substitute user do”，或者，更恰当地，“super user do”。用`sudo`执行一个命令会使用 root 账户权限。当然，使用之前需要 administrator 账户（管理员账户）的授权（如输入密码）。

默认情况下，任何管理员账户都可以使用`sudo`来获取 root 权限，甚至当 root 账户在图形界面被禁用的情况下，`sudo`依然有效。这个命令是很多情况下我们不得不使用 Terminal 的原因，——同样也是给每个用户管理员身份的危险所在。不过，你可以调整`sudo`的配置文件，来限制它的使用。
    
    bogon:~ renfei$ cat secret.txt
    cat: secret.txt: Permission denied
    bogon:~ renfei$ sudo cat secret.txt
    Password:
    This is the contents of the secret.txt text file that the user account renfei does not normally have access permissions to read. However, because he is an administrative user, she can use the sudo command to envoke root user access and read the contents of this file.
    

**提示**：如果由于你忘了使用`sudo`而导致命令行返回一个错误，只需输入`sudo !!`就可以用`sudo`来执行上一条指令。

记住，权力越大责任越大。不恰当地使用`sudo`可以轻易破坏你的系统设置。命令行只会在你第一次执行严重破坏性行为之前提示你，之后，它就会假设你清楚自己正在干什么。如果你只掌握三条使用命令行的准则，那将是：总是仔细检查你的命令；总是使用Tab completion来帮助你避免拼写错误；使用`sudo`之前，总是仔仔细细检查你的命令。

#### 使用 sudo 切换 Shell

如果你是一个管理员用户，你需要执行很多条需要 root 权限的命令，你可以临时切换整个命令行 shell 来取得 root 级别的访问权限。方法就是先输入`sudo -s`，回车后再键入你的密码。

## 其他Command-Line技巧提示

  * 输入命令`open .`可以用 Finder 打开当前的位置。
  * 在 Terminal 的偏好里面可以设定它的外观和风格。
  * 中止一个错误的或者发疯的命令，可以使用组合键control + C。
  * 你可以在执行前编辑命令，只需要使用箭头和键盘上的其他字母。
  * 没有输入任何命令时，你可以用▲和▼来浏览历史命令。同样可以编辑和再次执行。
  * 你也可以使用`history`命令查看历史记录。
  * 你可以使用组合键control + L清屏。
