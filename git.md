# Git



## git网络代理设置

git config --global https.proxy

示例:git config --global https.proxy http://10.1.249.61:3128

## git新建仓库后将本地文件提交

```xml
$ git remote add shrio  https://github.com/gepengfeicode/rabbitmq.git
fatal: remote shrio already exists.<!--这句话的意思是shrio文件夹不存在 需要使用git push命令将本地仓库提交到git仓库的master分支上-->
git push -u 提交的文件名称 master
把本地库的内容推送到远程，使用 git push命令，实际上是把当前分支master推送到远程。

　　由于远程库是空的，我们第一次推送master分支时，加上了 –u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。推送成功后，可以立刻在github页面中看到远程库的内容已经和本地一模一样了，上面的要输入github的用户名和密码如下所示：
```

## 将更新后的文件放入到github上

　git push 文件名master

## 将内容提交至Github上

 git remote add god_project https://github.com/gepengfeicode/god_project.git  链接上github

git push simple_shiro master  提交的项目名称

## 删除github上的文件

git rm -r --cached fileName

 git commit -m '删除了文件fileName'        # 提交,添加操作说明





## git常用命令

1.git init 生成git仓库

git init 

2.git add添加git文件

git add filename

3.git commit 提交文件

git commit -m'' 提交记录描述''

git diff filename 查看本次修改与上次修改的内容

4.git status  查看文件提交状态   modified 做了修改未提交

git status

5.git log 查看提交记录  增加 --pretty=oneline 参数可缩略

git log --pretty=oneline

6.git reset --hard HEAD~1 回退(只能回退当前版本不能回滚git仓库)

7. git checkout -- readme.txt 修改文件后 未执行add命令 使用此操作可将文件内容修改到修改前的内容
8. git reset HEAD readme.txt  执行完add命令后文件进入缓存区执行此命令可将文件在缓存区的内容消除

```tex
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/gepengfeicode/git_school.git
git push -u origin master
```

```tex
查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
```

