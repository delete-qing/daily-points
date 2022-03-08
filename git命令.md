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

9. git merge --abort 跳过合并

10. git reset origin/task-1425 合并远程代码 保留本地修改 这是有冲突的时候用的

11. 回退版本

- git reset --hard d514bdff 【d514bdff 版本号】
- git push -f
- git pull

12. git remote prune origin 清除远程分支

13. git push --delete origin task-8 删除远程分支

14. git branch -D test 删除本地分支

15. git remote --v 查看仓库

16. git branch -vv 查看分支关联的仓库

17. git remote remove 【仓库名】 删除仓库

18. git log 查看 git 提交记录

19. git merge master 合并分支 当前分支例如为 task-1 需要合并 master 分支上面的代码 那么就把分支切换到 task-1 上面 然后执行命令

20. git checkout -b task-999 origin/task-179 本地分支关联远程分支

21. cat ~/.ssh/id_rsa.pub 查看 ssh
