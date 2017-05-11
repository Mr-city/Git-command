# Git-常用命令

![git](git.png)

### [命令来自--廖雪峰Git 教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000)

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
git reset 回退版本   
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
总之，就是让这个文件回到最近一次git commit或git add时的状态。1
```





