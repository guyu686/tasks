# git学习笔记

[git下载，配置及上传文件](#git下载，配置及上传文件)

[git提交问题及优化](#git提交问题及优化)

[git指令积累](#git指令积累)



## git下载，配置及上传文件

1. GitBash 下载：http://www.git-scm.com/download/，安装基本默认，记得配置环境变量

2.  注册 github：关注用户名 username，邮箱 email，
    新建仓库：关注仓库 repertory_url
3.  git 命令：git config -l，查看系统配置 git config --system -l，查看个人配置 git config --global -l
4.  配置用户名和邮箱：git config --global user.name “用户名”
    git config --global user.email “邮箱”
5.  生成自己的私钥/公钥：ssh-keygen -t rsa，生成文件在 C/用户/ziy/.ssh
    在 github_上进行绑定(公钥)
    测试绑定是否成功：ssh -T git@github.com
6.  创建全新仓库：初始化 git 项目：git init(生成.git 隐藏文件)
    克隆远程仓库：git clone repertory_url
    有 git 项目后，上传: git add，添加文件到暂存区 stage
    git commit 提交暂存区内容到本地仓库，同时附上提示信息
    查看文件状态：git status [filename]
    最后 git push 

参考视频： https://b23.tv/5F0ld6z

---
## git提交问题及优化
  思考：我认为Git Bash提交比较麻烦————因为是命令行传输指令，这就要求我们准确记忆or查找并输入每个指令，造成了较大的工作量；另外，在使用git bash传输时可能会遇到由于防火墙或代理造成网络不稳定的问题（类似情况见[问题解决记录](https://github.com/guyu686/tasks/blob/main/%E9%97%AE%E9%A2%98%E8%A7%A3%E5%86%B3%E8%AE%B0%E5%BD%95.md)的*二阶段问题解决*）
  
  优化：
  1. TortoiseGit的使用：图形化用户界面且专为Windows设计，下载安装使用参考[TortoiseGit](https://b23.tv/MHfv9i8)<!--官网有汉化插件下载和操作都简单-->
  2. GitHub Desktop的使用：图形化用户界面，使用参考[GitHub Desktop](https://b23.tv/6VdBzyu)<!--目前我还没找到汉化版但操作同样简单-->



## git指令积累

### 初始化与克隆

- “git init”:在当前目录创建一个新的本地Git仓库。
- “git clone<repo-url>”:将远程仓库克隆到本地。

---

### 基础操作

- git add <file>：将文件添加到暂存区。
- git add . 或 git add -A：添加所有变更文件。
- git commit -m "提交信息"：将暂存区的变更提交到本地仓库。
- git commit -am "提交信息"：直接提交已跟踪文件的修改，无需先使用 git add。
- git status：查看工作区和暂存区的状态。
- git diff：查看未暂存的变更内容。
- git diff --cached：查看已暂存的变更。

---

### 分支管理

- git branch：列出所有本地分支。
- git branch -a：查看所有分支，包括远程分支。
- git branch <branch-name>：创建新分支。
- git checkout <branch-name>：切换到指定分支。
- git checkout -b <branch-name>：创建并切换到新分支。
- git merge <branch-name>：将指定分支合并到当前分支。
- git rebase <branch-name>：将当前分支的提交移到目标分支的顶部。
- git branch -d <branch-name>：删除本地分支。
- git branch -D <branch-name>：强制删除未合并的分支。

---

### 远程仓库操作

- git remote -v：查看远程仓库地址。
- git remote add <name> <url>：添加远程仓库。
- git push <remote> <branch>：将本地分支推送到远程仓库。
- git push -u origin main：首次推送时设置上游分支。
- git push --force：强制推送（谨慎使用）。
- git pull <remote> <branch>：拉取远程分支并合并。
- git pull --rebase：拉取时使用变基而非合并。
- git fetch <remote>：下载远程仓库的变更，但不合并。

---

### 撤销与回退

- git restore <file>：撤销工作区的修改（未 add 的变更）。
- git reset <file>：将文件移出暂存区，保留工作区修改。
- git reset --hard HEAD：丢弃所有未提交的变更（慎用）。
- git reset --hard <commit-id>：回退到指定提交（会丢失之后的提交）。
- git revert <commit-id>：创建一个新提交来撤销指定提交（安全回退方式）。

---

### 日志与历史

- git log：查看提交历史。
- git log --oneline：简洁模式查看提交历史。
- git log --graph：图形化显示分支。
- git show <commit-id>：查看某次提交的详细信息。
- git blame <file>：查看文件的修改记录（按行显示作者）。

---

### 暂存临时工作

- git stash：临时保存未提交的变更。
- git stash pop：恢复最近暂存的变更。
- git stash list：查看所有暂存记录。

---

### 标签管理

- git tag：列出所有标签。
- git tag -a v1.0 -m "版本说明"：创建附注标签。
- git push origin --tags：推送所有标签到远程仓库。

---

### 配置相关

- git config --global user.name "姓名"：设置全局用户名。
- git config --global user.email "邮箱"：设置全局邮箱
- git config --list：查看当前配置



