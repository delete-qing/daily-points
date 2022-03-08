## 简单基本流程

#### 大体步骤

1. 在 github 上新建项目

2. 在本地新建一个文件夹在 webstorm 中打开

3. 在 webstorm/viscode 中打开并且新建文件 .gitignore 文件

4. 在.gitignore 文件写入.idea/.vscode 过滤文件

5. git remote add origin +（这里是 git clon 的地址 如果新建文件没有写 README 文件 可以在文件提示下找到 git 关联的地址）关联远程代码仓库

6. git add . 这里是查阅文档了解,应该是没有跟踪文件,所以要 add 下跟踪文件

7. git commit -m “第一次提交主线的文件” (提交文件)

8. git push 提交到远程,到这里主线已将建立完成主线 **_master_**

#### 关于分支

9. **_git checkout -b oneLine_** 在本地新建一个分支名字为 **_oneline_**
   ，这里若是名字命名错了 **_git branch -m oldname newname_** 修改本地的名字

10. git push 推送到远程分支，这里会有提示要远程关联一个 oneline 的分支
    git push --set-upstream origin oneline

11. 输入这行命令 git push --set-upstream origin oneline 刷新远程 这里就可以看到远程也有 online 这个分支了

12. git checkout oneline 切到这个分支 新建文件 添加所需要上传的文件

13. git add .

14. git commit -m "第一次提交分支"

15. git push 这是新建的第一个分支

#### 切分支

16. git checkout master 切到主线

17. git checkout -b twoline 从主线切出来 新建第二个分支 这是在本地新建的分支 命名为 twoline

18. git push 推送到远程

19. git push --set-upstream origin twoline 关联远程分支 twoline

20. 这个时候可以把需要的上传的文件放到 twoline 这个分支下

21. git add. 添加到暂存区

22. git commit - m "第一次提交第二个分支的数据"

23. git push 推送到远程

24. git checkout master 切回主线

#### 合并 删除 分支

24. git merge oneline 合并第一个分支到主线

25. git add .

26. git push

27. git branch -D --delete oneline 删除本地分支 oneline

28. git push origin --delete oneline 删除远程分支 oneline

#### 合并分支

首先，你可能处于一个非 develop （开发）分支，确定已提交所有的本地改动，并推送（push）到了远程，假设当前分支名为 feature-purchase

然后，切到开发分支并拉去最新代码： **_git checkout develop && git pull_**

合并刚才的功能分支：git merge feature-purchase
（如果提醒没有该分支，则直接合并该功能分支的远程版本：git merge origin/feature-purchase

注：合并分支操作会产生一条提交信息，一般使用其默认的提交信息即可。确定光标在终端（而不是代码文件），按下 ESC 键，输入 :wq 安全保存并退出。

最后推送开发分支至远程：git push

#### 切换代码源

1. 推代码 拉取 master 代码

2. 切到功能分支 git pull

3. 重命名当前仓库的代码源为 【name】 git remote rename origin 【name】

4. 添加 【新的例如：maikeos】 的代码源并命名为【origin 默认的名字】 git remote add origin 【远程仓库的地址】

5. 查看当前代码仓的所有远程仓库 git remote -v

6. 在其他分支操作时，第一次推送请使用（[branchName]为分支名），之后即可使用 git push -u origin task-8

#### 换仓库推代码/关联多个代码仓

1. 切到关联别的仓库的代码 例如：git checkout j-test 这个【j-test】是关联的别的仓库的代码

2. git merge test

3. 推送代码 git push jinjia HEAD:test 这个【jinjia】相当于【origin】是仓库的名称 【HEAD:test】推送代码到最新的代码到【test 这个 test 是推送到劲嘉仓库的那个分支 test 可修改】

#### 合并冲突提示

```js
git merge test
Auto-merging src/page/quotation/quotation.jsx
CONFLICT (content): Merge conflict in src/page/quotation/quotation.jsx
Automatic merge failed; fix conflicts and then commit the result.


Accept Current Change  接受当前的变化
Accept Incoming Change 接受传入的更改
Accept Both Change  接受两者的改变
Compare Changes  比较变化

其中<<<<<<< Updated upstream到=======之间的代码是你拉取的别人的代码，=======到>>>>>>> Stashed changes是你自己本次修改的代码
```

##### 解决冲突

首先找的要合并的分支 并且切到要被合并的分支 （要合并代码到 test 但是发现合并到 test 上有冲突）那么就要把要合并的分支 merge 下 找到冲突 并且解决

之后直接 commit push 就可以了
