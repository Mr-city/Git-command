# Git-常用命令

![git](git.png)

[git教程之--廖雪峰](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000)
>**git init**

```
创建版本库  
命令把这个目录变成Git可以管理的仓库
```
<br/>

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

>**git commit -m "content"**  
>**git commit -am "content"**

```
文件的最后提交 -m 是提交说明 必须写
-am 直接提交修改的文件 不用在add到暂存
```

<br/>

>**git status**  
>**git diff**

```
git status 时刻掌握仓库当前的状态  
git diff 查看修改的内容 
```
<br/>

>**git log**  
>**git reset --hard HEAD^**

```
git log查看提交日志  

git reset 回退版本   
*HEAD 当前版本  
*HEAD^ 
```



![ls](ls.png) 
