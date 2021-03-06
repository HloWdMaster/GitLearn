#### git初始化设置

```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

#### 创建版本库

```
$ git init
$ git add <file>
$ git commit -m "注释" 
```

#### 创建远程分支

```
1.github创建远程分支
2. $ git fetch同步远程分支
3. $ git checkout -b dev origin/dev	创建本地分并关联远程分支

```

#### 多人协同工作

查看远程库信息，使用`git remote -v`；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用`git push origin branch-name`，如果推送失败，先用`git pull`抓取远程的新提交；

在本地创建和远程分支对应的分支，使用`git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用`git branch --set-upstream branch-name origin/branch-name`；

从远程抓取分支，使用`git pull`，如果有冲突，要先处理冲突。

#### 标签

```
标签与commit绑定
命令git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；
命令git tag -a <tagname> -m "blablabla..."可以指定标签信息；
命令git tag可以查看所有标签。
```

#### 操作标签

```
命令git push origin <tagname>可以推送一个本地标签；
命令git push origin --tags可以推送全部未推送过的本地标签；
命令git tag -d <tagname>可以删除一个本地标签；
命令git push origin :refs/tags/<tagname>可以删除一个远程标签。
```