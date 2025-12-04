---
title: Git 常用指令
timestamp: 2025-12-05 01:00:00+08:00
tags: [编程, git]
description: git 的常用指令。
---

## 创建
在当前目录下创建一个新的、空的 Git 版本库，记得写 .gitignore 文件
```
git init
```

## 暂存
将工作区的文件添加到暂存区
```
git add .
```

## 提交
将暂存区的文件存到本地仓库
```
git commit -m "做了什么什么"
```

## 远程
在本地仓库创建一个名为 origin 的远程仓库，并指向提供的 url
```
git remote add origin <url>
```

更新远程仓库
```
git push origin <branch>
```

获取远程仓库的最新版，合并到自己的本地分支
```
git pull
```

`git pull` 实际上是 `git fetch` 和 `git merge`的组合。

## 分支
查看本地分支
```
git branch
```

查看远程分支
```
git branch -r
```

创建新分支，但停留在当前分支
```
git branch <branch>
```

创建新分支，并切换到该新分支
```
git checkout -b <branch>
```

切换分支
```
git checkout <branch>
```

合并某分支到当前分支
```
git merge <branch>
```

合并某 commit 到当前分支
```
git cherry-pick <commit-id>
```
```
git cherry-pick --continue
```

删除本地分支，要先切换到其他分支上
```
git branch -d <branch>
```

## 其他
克隆项目
```
git clone <url>
```

配置提交代码时的用户信息
```
git config --global user.name "xxx"
```
```
git config --global user.email xxx@gmail.com
```

显示本地更新历史记录，最新的提交会在最顶部
```
git reflog
```

将修改合并入上次提交，有远程仓库时谨慎使用
```
git commit --amend
```

先检查远程分支是否有其他人新的提交，若无，将强制推送，覆盖上次提交记录
```
git push --force-with-lease origin <branch>
```

撤销前三次提交，但修改还在暂存区，最后记得 commit 一下
```
git reset --soft HEAD~3
```

查看已配置的用户名和邮箱
```
git config user.name
```
```
git config user.email
```

## 链接
**.gitignore 模板**  
https://github.com/github/gitignore

**官网**  
https://git-scm.com/