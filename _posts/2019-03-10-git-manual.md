---
layout:     post                    # 使用的布局（不需要改）
title:      git manual               # 标题 
subtitle:   how git works?  #副标题
date:       2019-03-10              # 时间
author:     羽聪                      # 作者
header-img: img/git_post.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - git
---

## git 常用指令大全

创建本地库：`git init`

查看当前状态：`git status`

添加至缓冲区：`git add <file name>`

上传：`git commit -m "xxx"`

上传至远程库：`git push origin master`

未add前，撤销：`git checkout -- <filename>`

add后，撤销：`git reset HEAD <filename>`，随后`git checkout -- <filename>`

把误删的文件恢复到最新版本：`git checkout -- test.txt`

版本回退：`git checkout -- test.txt`

查看提交历史：`git log`

查看命令历史：`git reflog`

查看分支：`git branch`

创建分支：`git branch <name>`

切换分支：`git chechout <name>`

创建+切换分支：`git checkout -b <name>`

合并某分支到当前分支：`git merge <name>` （删除分支后不会丢掉分支信息 `git merge --no-ff -m <name>` ）

删除分支：`git branch -d <name>`

强行删除分支：`git branch -D <name>`

查看分支合并图：`git log --graph `

保存当前工作现场：`git stash`

恢复原先工作现场：`git stash apply`

删除工作现场：`git stash drop`

查看历史工作现场：`git stash list`

恢复并删除工作现场：`git stash pop`

查看远程库信息：`git remote -v`



## 多人合作

```flow
st=>start: Start
op1=>operation: git push origin <branch-name>
cond1=>condition: if succeed?
op2=>operation: git pull
cond2=>condition: if "no tracking information"?
op3=>operation: git branch --set-upstream-to <branch-name> origin/<branch-name>
e=>end
st->op1->cond1
cond1(yes)->e
cond1(no)->op2->cond2
cond2(yes)->op3->op2
cond2(no)->op1
```

