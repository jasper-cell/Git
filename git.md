# git

初始化一个git仓库：使用**git init**命令

添加文件到Git仓库分为两步：

1. 使用**git add<file>**，注意，可反复多次使用，添加多个文件
2. 使用命令**git commit -m"description"**进行提交到仓库中
3. 要随时掌握工作区的状态，使用**git status**
4. 如果**git status**告诉你文件被修改过，可以使用**git diff**查看被修改的内容
5. HEAD指向的版本就是当前版本，因此Git允许我们在版本的历史之间穿梭，使用命令**git reset --hard commit_id**.
6. 穿梭前，用git log 可以查看提交历史，以便确定要回退到哪个版本，也可以使用简单模式的**git log --pretty=oneline**
7. 要重返回来，用**git reflog**查看历史命令，以便确定要回到未来的哪个版本。
8. 当乱改了工作区的某个文件内容，想直接丢弃掉工作区的修改时，可以使用**git checkout -- file**
9. 当修改了工作区文件，并且还发到暂存区的话，此时就需要，进行git reset HEAD <file>，回到工作区，清除暂存区的修改，然后再利用**git checkout -- file** 进行工作区的清除
10. git checkout的本质是利用版本库中的版本替换掉工作区的版本，无论是在工作区进行修改或者删除，都可以一键还原工作区。
11. git rm用于删除一个文件， 如果一个文件已经被提交到版本库，
12. **git remote add origin git@server-name:path/repo-name.git**,关联一个远程仓库。
13. 使用**git push -u original master**第一次推送master分支的所有内容，此后每次本地提交只需要使用**gait push original master**推送最新修改。
14. git鼓励大量使用分支:
- 查看git分支: git branch
- 创建分支: git branch <name>
- 切换分支: fit checkout <name> 或者 git switch <name>
- 创建加切换分支: git checkout -b <name> 或者 git switch -c <name>
- 合某分支到当前分支: git merge <name>
- 删除分支: git branch -d <name>
