把一个已有的本地仓库与之关联
git remote add origin git@github.com:michaelliao/learngit.git
把文件添加到仓库：
git add readme.txt
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
用git log可以查看提交历史，以便确定要回退到哪个版本。
用git reflog查看命令历史，以便确定要回到未来的哪个版本。
git log --graph --pretty=oneline --abbrev-commit
git mv 就相当于运行了下面三条命令：
mv README.txt README
git rm README.txt
git add README
通过push操作把本地分支推送到远程
git push origin master
git 中文支持
https://www.cnblogs.com/yanzige/p/9810333.html
1、运行Git Bash窗口，在该窗口导航条（即最上面）右键，选择Options−>Text，找到下面两处
　　Locale:选择 zh_CN 
　　Charector set:选择 UTF-8 
2、到Git Bash命令窗口输入如下设置命令语句
git config --global i18n.commitencoding utf-8  --注释：该命令表示提交命令的时候使用utf-8编码集提交
git config --global i18n.logoutputencoding utf-8 --注释：该命令表示日志输出时使用utf-8编码集显示
export LESSCHARSET=utf-8  --注释：设置LESS字符集为utf-8
git gui 文件乱码
修改编码集
点击 Edit --->Options...
找到 Default  file content encoding  ， 点击 Change
Git pull
push前先将远程repository修改pull下来
git pull origin master
git push -u origin master
若不想merge远程和本地修改，可以先创建新的分支：
git branch [name]
然后push
$ git push -u origin [name]
