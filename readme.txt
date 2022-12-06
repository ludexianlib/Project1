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

test sequence: this is master branch;