把文件添加到仓库：
git add readme.txt
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
用git log可以查看提交历史，以便确定要回退到哪个版本。
用git reflog查看命令历史，以便确定要回到未来的哪个版本。
git mv 就相当于运行了下面三条命令：
mv README.txt README
git rm README.txt
git add README
