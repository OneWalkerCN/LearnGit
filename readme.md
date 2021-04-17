# 这是一个git学习笔记

> git是一个免费开源的好工具
> 我们都喜欢git，所以要学习它

## 创建、修改、添加文件

* git init --创建仓库

* git add <文件名> --添加文件到仓库

* git commit -m "<文件的提交细节>" --提交文件

> 为什么有了add为什么要commit文件，因为commit可以提交好多个文件所以可以用add添加多个文件再commit

## 查看文件状态

* git status --查看仓库的状态

* git giff --查看具体修改内容

* git log --查看版本历史记录（--pretty=oneline参数更好的观看）

## 回退上一个版本

> HEAD指向的版本就是当前版本

* git reset --hard HEAD^

> 上一个版本 HEAD^ 
> 上上个版本 HEAD^^
> 上第十给版本 HEAD~10

## 指定到一个版本

* git reset --hard <版本号（前几位就好）>

* git reflog --查看每一次命令

> git reflog查看历史指令可以找到每次commit的版本号

## git提交过程

工作区 --git add-->stage(暂存区)--git commit-->分支

## 撤销修改

* git checkout --file 丢弃工作区修改（没有提交到暂存）

* git reset HEAD <文件名> 撤销暂存区修改，放回到工作区（已经提交到暂存但还没commit）

## 删除文件

* git rm 从库中删除文件 然后 git commit

* git checkout --<文件名> 版本库替换工作区的文件

## 远程连接到GitHub

* ssh-keygen -t rea -C "<你的邮箱>"

> 在用户主目录（默认C:\Users\Administrator\.ssh）找到`id_rsa.pub`公钥,将其内容填到Account settings->SSH keys->Add SSH Key

> 每台机器都可以将自己的公钥提交到一个账户，这样可以多台机器公用一个远程账户

* git remote add <远程库名> <远程库地址>  添加远程库

* git push -u <远程库名> <分支名称> 将本地分支与远程库分支关联

> 做完以上工作后，远程库和本地库就已经同步了

* git push <远程库名> <分支名称> 提交本地修改到GitHub

## 删除远程库

* git remote -v 查看远程库信息

* git remote rm <远程库名> 删除远程库与本地库关联