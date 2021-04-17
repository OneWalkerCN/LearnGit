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

工作区 --<git add>-->stage(暂存区)--<git commit>-->分支

## 撤销修改

* git checkout --file 丢弃工作区修改（没有提交到暂存）

* git reset HEAD <文件名> 撤销暂存区修改，放回到工作区（已经提交到暂存但还没commit）

