## Mac

首推当然还是MacOS，当然可能受限于条件，没能拥有Mac机器。

[Hackintosh](https://hackintosh.com/)也是一种可能的选择。


## Linux

首推Arch Linux，用过绝对欲罢不能。用Arch很多人会推荐Manjaro，原因当然是Arch难装，然而我不推荐，因为Manjaro是基于Arch，而不是Arch，软件仓库是有区别的，有点像ubuntu和debian的感觉。而Arch拥有最多最新的软件。

事实上Arch是需要自己安装一遍的，因为在这个过程你会学到很多，并且如果你不能handle安装的话，Arch出问题，你也可能搞不定，所谓能力多大，责任多大，Arch给你自由，你也应该有相应的能力。

如果要先上手，我推荐[Antergos](https://antergos.com/)，因为Antergos完全就是原生的Arch，它只不过是做了一个installer而已。


## Windows

Windows也是推荐的，毕竟国内的环境，有时候不投降不行。而用惯命令行用Windows会很不爽。


我试用了WSL，把Ubuntu子系统换成了Arch，但是我生成的ssh key，无法连接到github，用`ssh -T git@github.com`测试，根本找不到github在那里，所以很可能在WSL是无法ssh的，要在Windows主系统下才行。这让我很不爽，而弃坑（如果我错了请指出）。


传统做法，当然你可以用虚拟机，WSL之所以受欢迎就是不想切换到虚拟机，然而WSL必定也没有虚拟机这种全面支持，必定也有些限制。


那么就只能找原生的bash了，[Git for Windows](https://gitforwindows.org/)就提供了一个bash；Emacs自身也是带有`shell`和`eshell`的，都可以用，但bash真的可以干的事情太少，太多的指令是缺失的，如果是Linux，不单单全，安装也容易，那么如果我们要用跑在Windows上的Bash的话，最重要的是一个所谓的【包管理器】，如同homebrew之于MacOS， apt之于Debian，pacman之于Arch等等。

我之前介绍过`Chocolatey`，但用着感觉不爽，因为要管理员身份去安装。我需要一个普通用户随时可以安装软件的管理器，于是我找到了`scoop`，它的理念很像homebrew的装瓶（bottle）和倾倒（poured），基本上下载压缩包，解压这样的绿色操作而已，而软件从那里下载等各种信息，存放于纯文本的json文件中。


安装很简单，参照[主页](https://scoop.sh/)，只需在Powershell中执行：

```
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```


然后就可以`scoop install cmder`安装非常好用的终端`Cmder`.

就可以在Cmder中使用CMD, Powershell，bash，WSL等，我基本上只用bash。

安装R:

```
scoop install r
```

像前面提到的`Git for Windows`，直接：

```
scoop install git
```


各种命令就可以安装了， 比如：

```
scoop install make
scoop install wget
scoop install vim
```


### 安装spacemacs

```
scoop bucket add extras
scoop install emacs

cd ~
git clone https://github.com/syl20bnr/spacemacs .emacs.d
```

