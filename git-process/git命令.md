## git 命令

1. git cherry-pick <commitHash>
   git cherry-pick 命令的作用，就是将指定的提交（commit）应用于其他分支

2. git checkout feature-project-manage 切换分支

   - git pull
   - git add .
   - git commit -m "文字"
   - git push

3. git commit 后面没有写提交信息
   输入 i （即 insert） 输入备注信息，输入完成之后 点击 esc ,然后输入：wq 就退出回到命令界面了

4. $ git branch -a 列出所有本地分支和远程分支

5. $ git branch 列出所有本地分支

6. $ git branch -r 列出所有远程分支

7. git merge feature-purchase-new 合并分支到当前分支

8. $ git cherry-pick [commit] 选择一个 commit，合并进当前分支
   这个是切换到当前打分支区拉取别的分支的提交

9. git merge --abort  跳过合并

10. git reset origin/task-1425  合并远程代码 保留本地修改 这是有冲突的时候用的

