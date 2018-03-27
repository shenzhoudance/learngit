Git is a version control system.
Git is free software.
Git has a mutable index called stage.
Git tracks changes of files.

1.
git add readme.txt
git commit -m "wrote a readme file"

初始化一个Git仓库，使用git init命令。
添加文件到Git仓库，分两步：
第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；
第二步，使用命令git commit，完成。

2.
git status
git diff readme.txt 

git add readme.txt

要随时掌握工作区的状态，使用git status命令。
如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

3.
切换不同版本
git reset --hard commit_id
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

4.
git checkout -- readme.txt
git checkout -- file可以丢弃工作区的修改：
2.假如已经add了，那么可以用命令git reset HEAD file可以把暂存区的修改撤销掉（unstage）
 git reset HEAD readme.txt
 git checkout -- readme.txt
 3.已经提交了不合适的修改到版本库时，想要撤销本次提交，请看上一节 3.  git reset --hard commit_id

 5.
 一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit：
 另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
 git checkout -- test.txt