# Windows-MacOS-pymol-
由于目前PyMol应用程序已经被Schrödingerg公司收购，因此想要使用最新版本的PyMol是需要付费的。但PyMol最早是由Warren Lyford DeLano 开发的，在其生前一直坚持开源使用PyMol。所以公司也保留开源版本的PyMol供用户使用。在PyMol 2.1版本之前的版本是可以从SourceForge下载到的，然而后面更新的版本都转移到了GitHub。因此本文记下了本人尝试成功的安装开源pymol的方法供大家参考，有兴趣的小伙伴可以试一下。


##01 Windows

1. Install anaconda

不安装任何版本的python， 使用anaconda自带的python版本，

检查Anaconda 自带python 版本与需要安装的pymol所需版本是否相符合，如不符合，需要为pymol创建所需的python版本，如：

conda create -n python37 python=3.7  #来创建名为"python37"的环境

conda activate python37

在python37 环境下安装pymol

 

2. 从此网站下载免费开源的pymol版本（对应python版本）

https://www.lfd.uci.edu/~gohlke/pythonlibs/  

（Archived: Unofficial Windows Binaries for Python Extension Packages）

 

3. Pymol包的安装

① 安装Pymol之前，先运行pip install pmw和pip install numpy来安装pmw和numpy

②anaconda prompt  转到下载的Pymol包所在位置，输入pip install pymol-2.5.0a0-cp37-cp37m-win_amd64.whl (对应python 3.7 version)


###02 MacOS


这个方法是参考来自原文CSDN博主原文链接：https://blog.csdn.net/weixin_45725149/article/details/123698134，已经在MacBook Pro M2 芯片上试过，成功安装。

1，可以首先从官网安装最新版本的PyMol，通过官网下载.dmg文件即可，然后按照标准程序拖到/Applications里面即可，但此版本打开程序时会显示没有激活的licence，我们暂且可以不用管，直接关掉PyMol程序就可以。
PyMOL | pymol.org    https://pymol.org/2/

 2，我们可以同时
通过MacPorts （我已经尝试过这个方法，能work，如果遇到任何问题，根据提示来安装额外的软件包即可，直至成功安装Macports）
The MacPorts Project -- Home
The MacPorts Project is an open-source community initiative to design an easy-to-use system for compiling, installing, and upgrading either command-line, X11 or Aqua based open-source software on the Mac OS X operating system.
https://www.macports.org/
 或者homebrew
The Missing Package Manager for macOS (or Linux) — Homebrew
The Missing Package Manager for macOS (or Linux).
https://brew.sh/
直接安装open-source版本的PyMol。
### MacPorts
sudo port install pymol
#### Homebrew
brew install brewsci/bio/pymol 
3，最后我们可以通过which pymol找到open-source的PyMol所在文件夹，如/opt/local/bin/pymol。随后使用以下代码：
sudo cp /Applications/PyMOL.app/Contents/MacOS
 就可以将商业版的PyMol可执行程序替换为开源版本的，而不需要licence。
 
（至于如何安装MacPorts和homebrew可能碰到的问题，可以在CSDN上面自己查找。后续我们也可以再说。）
