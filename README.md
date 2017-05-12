# Git-常用命令

![git](git.png)

<br/>

[![NetflixOSS Lifecycle](https://img.shields.io/badge/命令来自-廖雪锋的Git教程-brightgreen.svg)](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)


<br/>

>创建版本库  
>**git init**

```
命令把这个目录变成Git可以管理的仓库
```
<br/>

>添加到暂存区  
>**git add**  
>**git add** .  
>**git add** -u

```
把文件添加到暂存区  
git add [file] [file] 提交指定单个 或多个 文件  
git add . 提交当前目录下所有未跟踪的文件  
git add -u 在仓库任务目录下提交所有未跟踪的文件
```
<br/>


>文件提交  
>**git commit -m "content"**  
>**git commit -am "content"**

```
文件的最后提交 -m 是提交说明 必须写
-am 直接提交修改的文件 不用在add到暂存
```

<br/>

>查看状态-内容  
>**git status**  
>**git diff**

```
git status 时刻掌握仓库当前的状态  
git diff 查看修改的内容 
```
<br/>

>版本回退  
>**git log**  
>**git reflog**                     
>**git reset --hard HEAD^**

```
git log查看提交日志  
git reflog 查看命令历史，以便确定要回到未来的哪个版本  
git reset HEAD [file] 把暂存区的修改回退到工作区
git reset --hard HEAD 回退版本
- HEAD 当前版本  
- HEAD^  上一个版本
- HEAD^^  上上一个版本
- HEAD~100  多个版本
```

<br/>

><font style="color:#1b9c4b">撤销修改</font>  
>**git checkout -- [file]** 

```
命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
总之，就是让这个文件回到最近一次git commit或git add时的状态。
```

<br/>

>删除文件  
>**git rm [file]**

```
确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit。

用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，  
你会丢失最近一次提交后你修改的内容。
```

<br/>


>远程操作：关联 - 克隆 - 获取  
>**git remote add origin **  
>**git clone**  
>**git push origin master**  
>**git fetch**  
>**git pull**  

```
git remote add origin [地址]与已有的本地仓库与之关联
git clone [地址]从远程库克隆
git push origin master 推送到远程库
git fetch 相当于是从远程获取最新版本到本地，不会自动merge
git pull 相当于是从远程获取最新版本并merge到本地
```

<br/>

>创建分支  
>**git branch dev**  
>**git checkout dev**  
>**git checkout -b dev**  
>**git log --graph**  
>删除分支  
>**git branch -d dev**

```
git branch   查看分支
git branch dev 创建一个dev分支
git checkout dev 切换到dev分支
git checkout -b dev 简写：创建并切换到dev分支
git branch -d dev 删除dev分支
git log --graph 查看分支合并图
```

<br/>

>分支管理策略  
>**git merge --no-ff -m "merge with no-ff" dev**  

```
通常，合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息。  
如果要强制禁用Fast forward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息。
  
--no-ff参数，表示禁用Fast forward  

合并要创建一个新的commit，所以加上-m参数，把commit描述写进去

```


<br/>

>标签  
>**git tag v1.0**   
>**git tag -a v0.1 -m "version 0.1 released" 3628164**  
>**git tag -s v0.2 -m "signed version 0.2 released" fec145a**  
>**git tag -d <tagname>**  
>**git push origin --tags**


```
命令git tag <name>用于新建一个标签，默认为HEAD，也可以指定一个commit id；

git tag -a <tagname> -m "blablabla..."可以指定标签信息；

git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；

命令git tag可以查看所有标签。

命令git push origin <tagname>可以推送一个本地标签；

命令git push origin --tags可以推送全部未推送过的本地标签；

命令git tag -d <tagname>可以删除一个本地标签；

命令git push origin :refs/tags/<tagname>可以删除一个远程标签。
```
