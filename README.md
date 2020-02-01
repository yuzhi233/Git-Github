# Git-Github

小白老忘，记录一下，避免重复造轮子作无用功。。吐辽，针对自己的弱智行为 = =

首先注册啥的不说了不然我也上不了Github.

主要参考视频https://www.bilibili.com/video/av55780016（b站大法好）

​        参考文章 https://www.jianshu.com/p/3ef797fcb17d

### 第一步（当然默认GIT装完了）

要想本地和github完成连接，嗯，首先先创建连接（废话），这里是学人家用SSH创建一个本地连接SSHkey

运行**Git Bash**

在打开的窗口中输入如下指令

~~~bash
ssh-keygen -t rsa -C "邮件地址"// 填写你的github注册邮箱
~~~

![1580532043893](README.assets/1580532043893.png)

回车回车回车然后：

![1580532089757](README.assets/1580532089757.png)

表示生成完了，我在桌面bash的生成的文件默认路径也是桌面。

![1580532235265](README.assets/1580532235265.png)

这o.pub这个是我们需要的，右键notepad++打开复制一下SSHkey完事。

## 第二步

点击头像下的setting

![1580531663315](README.assets/1580531663315.png)





找到SSH and GPG keys 我已经创建了个，第一次的话new一个完事。

 ![1580531679311](README.assets/1580531679311.png)



Title下面起个标题（体现哪台电脑比较好）

![1580531728243](README.assets/1580531728243.png)



然后key就是第一步赋值的那个东西填进去。生成完就建立了本地电脑跟远程github的SSH连接。





### 第二步

先在Github端建立一个repository，简单8多说。

然后点击这里

![1580531449793](README.assets/1580531449793.png)

把右上角USE HTTPS改成 USE SSH  （好像大佬都说用SSH更好）HTTPS我没用也懒得知道咋用以后再说8.

然后复制完后找个你存放这个repository的文件夹，在文件夹里bash一下，输入

~~~bash
git clone git@github.com:yuzhi233/Git-Github.git #刚才复制的SSH链接
~~~

完了你会发现自动下载好了，并且里面已经有了隐藏的.git文件夹（貌似不需要git init了）

### 第三步

就是使用了。

小白为了防止头疼，记了几个常用且简单的，剩下的需要用到再google吧



**更新本地仓库**（如果你在云端编辑了，在本地的时候可以这样）

~~~git
git pull
~~~

查看暂存区状态

~~~git
git status
~~~

**添加到暂存区**

~~~git
git add .  #添加文件夹下所有文件
git add 文件名.后缀  #添加单个文件
~~~

有时候会遇到不小心添加错文件到暂存区，这时候

~~~git
git reset HEAD 取消所有暂存区文件
~~~

**提交**到工作区

~~~git
git commit -m '版本修改的信息'
~~~

查看git日志（commit的信息）

~~~git
git log
~~~

推送到Github

~~~git
git push
~~~

