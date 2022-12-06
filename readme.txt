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
git stash list
    git stash apply & git stash drop  == git stash pop
    git stash apply stash@{0}: 恢复指定的stash