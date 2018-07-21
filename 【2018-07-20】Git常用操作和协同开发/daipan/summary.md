[百度脑图](http://naotu.baidu.com/file/f5d606940e8add32a7b3804ea4c56ea9?token=2a41bd7c95854a12)

# 2.0 分享主题：Git常用操作和协同开发
1.配置alias\
    g = git\
    st = status\
    re = remote -v\
    ci = commit\
    cim = commit --amend\
    br = branch\
    mg = merge\
    rb = rebase\
    fe = fetch\
    li = log --oneline\
    lg = log --oneline --graph --decorate --all\
    rf = reflog\
    con = config --global -e\
    co = checkout\
    ln = log --author=daipan\
    fe = fetch\
    sa = stash\
    sap = stash pop\
    sal = stash list\
    s = push origin\
    l = pull origin\
    cp = cherry-pick\
    ps = push\
    pl = pull\
    sh = show\
    tr = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit\

2.Git常用指令：\
git status \
git diff (+具体的文件路径) 查看工作区的所有文件/具体某个文件修改了哪些\
git diff commit1 commit2 —stat      ——“查看两次提交之间的变动文件”\
git diff commit1 commit2 具体文件的src   ——“对比两次提交的某文件的变动”\
git log\
git reflog 可以查看到所有git操作记录。及时回滚也能查看到之前的提交。\
git li\
git tr\
git sh commidID 查看某次提交的修改内容\
git remote -v \
cat 文件名\

git branch new-branch  创建新分支\
git co 分支名\
git co -b  new-branch\
git co -b new-branch origin/remote-branch\
git br -d/-D branch\
git push origin  :remote-branch   —删除某个远程分支\

撤销\
git co .     —撤销所有的小改\
git co 具体的文件   ——撤销对该文件在工作区的修改\
从暂存区撤销到工作区\
git reset —hard 版本号 —— 回滚到上一个版本或具体的某一个版本\



临时存储
git stash \
git stash pop\
git stash list\


合并(后面的参数)\
git merge\
不怎么常用但是很重要\
git cherry-pick  commitID    ——表示当前分支合并某个具体的提交，并会生成新的提交id。\
应用场景：\

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/cherry-pick.png)

打tag\
git tag   —-查看所有tag\
git tag tagName   ——基于最新提交创建tag\
git tag -d tagName    ——删除tag \

提交暂存区、本地仓库、远程仓库\
![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/git-repository.png)

Add区别于联系\
git add -A  \
git add -u \
git add .\

git pull origin remote-branch\
=git fetch + git merge origin/remote-branch\

git push origin remote-branch  (当该远程分支在远程仓库不存在时，该命令就直接新建该远程分支)\

git push origin local-branch:remote-branch\
git pull origin remote-branch:local-branch\

[技术|25个 Git 进阶技巧](https://linux.cn/article-5418-shareweibo.html)\


问题：\
1. 如何撤销git pull的误操作？\
使用回滚可解决，但是回滚是否会影响到git stash的东西呢？\
2. git rebase \
3. git merge 是否后面跟commitid？试一下\
![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/git-experience.png)\

1.github origin和upstream的区别\
![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/upstream.png)

Fork后的git地址后加上自己用户名，克隆下来后r远程仓库也是自己github上的仓库
![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-1.png)

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-2.png)


![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-2.png)

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-3.png)

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-4.png)

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-5.png)

![image](https://github.com/daipanpan/Front-End-Sharing/blob/sharing/%E3%80%902018-07-20%E3%80%91Git%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C%E5%92%8C%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91/daipan/image/test-upstream-6.png)

总结git操作比较好的的连接：\
1.简书：https://www.jianshu.com/p/e2f553942317
