---
title: "Git"
date: 2021-03-09T21:02:47+08:00
tags:
- git 
- 学 
- 碎片

---

![](/img/git.jpg)

1.创建新仓库:

```bash
git init
```

2.克隆仓库:

```bash
git clone (local or internet)
```

3.工作流,三棵树:工作目录 add 暂存区 commit HEAD

4.添加和提交:

```bash
git add <filename>/git add . / git add *
git commit -m 'hint'
```

5.推送改动:

```bash
git push origin master
```

6.分支,绝缘开发,默认是master,假设有分支feature

```bash
#创建feature分支,并切换过去
git checkout -b feature
#切换回主分支
git checkout master
#删除分支
git branch -d feature
#推送分支
git push origin <branch>
```

7.更新与合并:

```bash
#更新本地仓库到最新
git pull
#将其他分支合并到你的分支,有可能发生冲突
git merge <branch>
#发生冲突时候检查
git diff <source branch> <target brach>
#改动文件,然后合并
git add <filename>
```

8.改动

```bash
#如何你本地操作失误,文件已经保存
git checkout <filename> #head区的内容替换到你本地的文件
#丢弃本地所有的改动,恢复原来的状态
git fetch origin
git reset --hard origin/master
```

