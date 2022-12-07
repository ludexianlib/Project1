git remote add origin xxx: 关联本地仓库
git push -u origin master: -u首次推送master分支（origin定义远程库名）
    git push origin master

git remote -v / git remote rm <name> 删除远程库（取消关联）

git checkout -b dev: 创建并切换dev分支  / git switch -c dev(new version)
    == git branch dev & git checkout dev / git switch master(new version)
git branch: 查看分支

git merge dev
git branch -d dev

git merge featurel: 在不同分支出现冲突解决
    // 手动修改要保存的内容

git merge --no-ff -m "Info" dev: 这种merge方式可查看删除的历史分支信息

git log --graph --pretty=oneline --abbrev-commit: 查看历史分支信息

git stash: 修改bug暂时储藏该分支，修复后合并
git stash list
    git stash apply & git stash drop  == git stash pop
    git stash apply stash@{0}: 恢复指定的stash

git cherry-pick "id": 修改后的部分matser分支通过提交的id复制到当前分支

git branch -D "branch": 强制删除未经过合并的分支

测试：多人协同
    git checkout -b dev origin/dev
    git push origin "branch": 推送分支
    1.git branch --set-upstream-to=origin/dev dev: 本地与远程分支链接
        git pull
        修改: git push origin <branch-name>
    
git rebase: 将本地未push的分支merge历史整理成直线

git tag <name> (id): 将历史commit id打标签
    git tag -a v0.1 -m "version 0.1 released" id
git show <name>