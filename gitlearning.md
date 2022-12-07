
---

# Git起步
1. git是分布式版本控制系统
2. git中的文件有三种状态：
- 已提交(committed):数据已经安全地保存在本地数据库中
- 已修改(modified):修改了文件，但还没保存到数据库中
- 已暂存(staged):对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中

---

# Git基础
1. 获取git仓库的两种方式：
- 将未进行版本控制的本地目录转换为git仓库
- 从其他服务器克隆一个git仓库
2. 使用命令 git add 开始跟踪一个文件
3. git status查看该文件已被跟踪，处于暂存状态  ->  Changes to be committed
4. 修改已跟踪内容，但还没放到暂存区  ->  Changes not staged for commit
5. git add是个多功能命令：
- 可以用它开始跟踪新文件
- 或者把已跟踪的文件放到暂存区
- 用于合并时把有冲突的文件标记为已解决状态等。
6. git diff 要查看尚未暂存的文件更新了哪些部分
7. git commit 提交命令  -a 把跟踪过的文件暂存并提交  -m ‘’命名
8. git rm 移除git文件
9. git mv git中文件改名
10. git log 回顾提交历史
11. git commit --amend  重新提交命令
12. git reset HEAD <file>... 取消暂存
13. git checkout --<file>...取消修改
14. git remote -v 查看远程仓库
15. git fetch <remote> 拉取远程仓库中更新的信息
16. git pull 自动抓取后合并远程分支到当前分支
17. git push <remote> <barnch> 将<branch>分支推送到<remote>服务器
18. git remote show <remote> 查看特定的远程仓库
- git remote rename <name1> <name2>  重命名远程仓库
- git remote remove <remote> 移除远程仓库

---

#Git分支
1. git branch <branch> 新建一个分支
2. git checkout <branch> 切换到某个分支
3. git checkout -b <newbranchname> 创建新分支的同时切换过去
4. git merge <branch> 将<branch>分支合并到当前分支中
5. git branch -d <branch> 删除分支

---

#Github
1. 派生：想要参与某项目，但是无推送权限
2. 派生后，会在自己的空间中创建副本，可以推送
3. git clone <派生链接> 将项目克隆到本地
4. git checkout -b <branch> 新建并切换到一个新的分支
5. 修改项目中的内容后，git commit -a -m 'instruction' 跟踪并提交修改到当前分支中
6. git push <remote> <branch> 将新分支推送到Github副本中
7. 在Github上点击pull request，给源项目创建拉取请求
