## 本地库创建

```
$ git init //把当前目录变成git可以管理的仓库
$ git add readme.txt //告诉git把文件添加到仓库
$ git commit -m "说明"//告诉git把文件提交到仓库
```

##  本地库提交远程库操作

```
$ git remote add origin git@github.com:TZSY/learning.git //把本地仓库和远程仓库关联
$ git push -u origin master//把当前分支master推送到远程
then
$ git push origin master//只要本地做了提交之后
```

##  远程库克隆到本地库操作

```
$ git clone git@github.com:TZSY/learning.git
```

​	克隆了一个本地库

##  本地库同步到远程库操作

```
$ git fetch <远程主机名>//将某个远程主机的更新全部取回本地
$ git fetch <远程主机名> <分支名>//取回特定分支
e.g. $ git fetch orgin master//取回origin主机的master分支
$ git log -p FETCH_HEAD//指某个branch（分支）在服务器上的最新状态
```

```
$ git pull origin master  -->

$ git fetch origin master
$ git merge FETCH_HEAD//将拉取下来的最新内容合并到当前所在的分支中

完整表示为：
$ git pull <远程主机名> <远程分支名>:<本地分支名>
如果远程分支是和当前分支合并，则冒号后面的部分可以省略
```

##  分支的概念

```
A----C----E（master）
 \
  B---D---F(dev)
```

ACE为master分支，ABDF为dev分支，他们的head指针分别指向E和F。

```
$ git checkout master //选择或者切换到master分支
$ git merge dev  //把dev分支合并到当前分支(master)
```

合并后

```
A---C---E---G(master)
 \         /
  B---D---F（dev）
```

G为合并的结果，可能有冲突。

ABDF仍然为dev分支，可以继续在dev的分支上进行开发，master分支同理。

```
A---C---E---G---H(master)
 \         /
  B---D---F---I（dev）
```

