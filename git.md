#### git 版本控制器

配置

```
git config --list  #查看配置的信息

git config --global user.name Nick #设置用户名

git config --global user.email nick_php@163.com #设置邮箱

git help config #获取帮助信息
```

普通操作

```
git status #查看文件状态

git add file #添加文件

git add . #添加当前目录下所有文件到版本库

git add -A ##添加所有文件到版本库

git commit -m '注释' #提交

```

新建仓库

```
mkdir www && cd www

git init #初始化

git status #查看文件状态

git add file #.或*代表全部添加

git commit -m "message"#此处注意乱码

git remote add origin git@github.com:username/project.git #关联远程仓库

git push -u origin master #第一次推送文件到远程仓库
```

克隆仓库

```
git clone https://github.com/Nick233333/gitbook.git #克隆远程仓库

git clone https://github.com/Nick233333/gitbook.git linux #克隆并指定目录名称
```

日志

```
git log #查看提交日志

git log --pretty=oneline #单行显示提交日志

git log --author=nick #查看指定用户的日志
```

分支

```
git branch #查看本地分支

git branch -r #查看远端分支

git branch -a #查看所有分支

git branch test #新建 test 分支

git checkout -b dev ##新建 dev 分支并切换

git checkout -b test dev #基于 dev 新建 test 分支，并切换

git merge test #将test分支合并到当前分支

git branch -m old new #重命名分支

git push origin branch #推送分支到远程

git branch -D branch #删除本地分支

git push origin :branch #删除远程分支

```

标签

```
git tag #列出现有标签

git tag v0.1#新建标签

git tag -a v0.1 -m 'my version 1.4'#新建带注释标签

git checkout tagname #切换到标签

git push origin v1.5 #推送分支到源上

git push origin --tags #一次性推送所有分支

git tag -d tag #删除本地 tag

git push origin :tag #删除远程 tag
```

关联远程仓库

```
git remote  #查看全部远程仓库

git remote add origin https://github.com/Nick233333/gitbook.git #添加本地仓库与远程仓库关联

git remote rename origin1 origin2 #重命名

git remote remove origin #取消与远程仓库关联

```