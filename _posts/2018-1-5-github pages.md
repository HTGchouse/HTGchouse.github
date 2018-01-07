---
layout: article
title:  "Github Pages的极简教程"
categories: rwd
image:
  teaser: website.jpg
  feature: file.jpg

---

先假设读者对ruby完全没有了解，仅对html有初步的了解

#### 本文标题所说的“极简”是基于下面的原则：

安装尽量少的软件
使用尽量少的命令
接触尽量少的概念

#### 下面开始一步步讲解Github Pages的使用流程：

###### 一、如果想在本地预览页面，跳过这步到二；如果不想在本地预览，则在windows下安装msysgit，最新版本为Git-1.7.9-preview20120201.exe，然后按照BeiYuu的博文里的过程配置git和github，再到四

如果你的系统是linux的，按照Git Hub官方帮助文件操作，然后跳到四。

如果想深入了解Git，请看10篇写给Git初学者的最佳教程。

###### 二、在windows下安装ruby环境。推荐安装RailsInstaller，里面包含了Ruby、Rails、Bundler、Git、Sqlite、TinyTDS、SQL Server support和DevKit。

不过最近的RailsInstaller里包含的ruby版本升到了1.9.3，如果以后要使用Octopress的话必须使用ruby1.9.2，建议使用以前的版本，我把以前的版本放到了这里。

###### 三、紧接着上一步，配置git和github

在RailsInstaller安装结束时安装程序会提示是否配置Git环境（这样的话给配置git和github带来极大的方便，又减少了几条命令）。选择”是”，然后出现下面的提示

<img src="https://htgchouse.github.io/images/cmd.png">

填写github注册时的用户名和邮箱，就完成了公钥和密钥的生成，在C:\Documents and Settings\用户名下，有个隐藏目录名为.ssh，id_rsa.pub文件就是公钥，id_rsa就是密钥。

在Github网站找到 “Account Settings” > Click “SSH Keys” > Click “Add SSH key”

<img src="https://htgchouse.github.io/images/github.jpg">

用文本编辑器打开id_rsa.pub文件，并把里面的内容（包括空格和新行）复制出来，填到Github的账户设置的SSH设置里。

<img src="https://htgchouse.github.io/images/key.jpg">

在开始菜单里找到RailsInstaller –> Git Bash，执行它，就打开了下面的命令窗口，以后的操作都是在这个窗口下进行的

<img src="https://htgchouse.github.io/images/cmds.jpg">

###### 注意: 在窗口里我们可以看到当前路径显示为/c/Sites，其实它表示的是C:\Sites，这个目录是RailsInstaller在安装的时候建的。
###### 用下面的命令测试一下git是否连接正常
###### ssh -T git@github.com

###### 四、安装jekyll和相关的包

稍微对配置做一下修改，把淘宝的镜像加到gem的镜像列表里

gem sources --remove http://rubygems.org/
gem sources -a http://ruby.taobao.org/
然后用gem sources -l看看现在源列表

*** CURRENT SOURCES ***

http://ruby.taobao.org
如果是上面这样就可以安装jekyll了

gem install jekyll
Jekyll需要用到directory_watcher、liquid、open4、maruku和classifier这几个包，用上面的命令可以自动安装。Jekyll默认用maruku来解析markdown语言，你也可以用别的程序来解析，比如rdiscount或kramdown，都给装上吧：

gem install rdiscount kramdown
以上命令涉及到gem install的时候，如果你用的是linux系统，就要用sudo gem install代替。

###### 五、建立github pages。

这一步是本文的重点，也是本文异于网络上其他文章的地方，我在这里用到了Github提供的Github pages generator的功能，减少了使用的命令数量，也绕开了远程代码库这个概念（省略了与git remote相关的操作，不过随着github使用的加深，这些概念也是不能避免的）

在github.com上创建代码库，比如新建一个名为example的代码库：登录到自己的Github账户，选择New repository

在线生成pages: 点Admin,接下来的页面可以不用填，直接点Create Page，马上会转到一个404页面，不要慌，要过一会系统才会帮你把网页生成好。

克隆自己的代码库

  git clone git@github.com:yanping/example.git
这样git会把存放在github上的代码库文件下载到本地的，生成名为example的目录。删除该目录下的index.html，这是系统生成的，不是我想要的页面，注意不要把.git目录删除，这是个隐藏目录，里面包含这个代码库的配置信息，以上的步骤都是为了得到这些配置信息且避免了使用命令。







