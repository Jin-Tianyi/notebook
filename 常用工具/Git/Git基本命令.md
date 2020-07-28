
##### 一、基本操作
```$git
git init #将一个文件夹初始化为git仓库  如将D:\porjects\test 初始化为Git仓库，cd D:\porjects\test后，git init
git clone [url] #将远程项目克隆到本地
git remote add [shortname] [url] #添加远程仓库
git status #命令用于查看项目的当前状态, -s 参数 精简形式
git add <file> <file> ... #将新建/修改暂存到缓存，git add .暂存所有
git diff #显示已写入缓存与已修改但尚未写入缓存的改动的区别
git diff --cached #查看已缓存的改动
git diff HEAD #查看已缓存的与未缓存的所有改动
git commit #提交改动到仓库 -m 参数添加提交信息 git commit -m 'first add'
git commit -a #无需git add 直接commit
git reset HEAD #用于取消已缓存的内容,如git reset HEAD readme.md
git rm <file> #删除文件
git rm -f <file> #删除之前修改过并且已经放到暂存区域的文件
git rm --cached <file> #把文件从暂存区域移除，但仍然希望保留在当前工作目录中
git rm –r *  #递归删除，慎用
git mv #移动或重命名一个文件、目录、软连接

```

##### 二、配置
```$git
# 提交用户的信息
git config --global user.name 'username'
git config --global user.email xxxxxx@qq.com
```

##### 三、分支管理
```$git
git branch #查看分支
git branch newbranch  #创建一个分支
git merge dev #合同分支，如要将dev分支合并到master分支，应先checkout master分支
git merge #合并多个
git branch -d dev #删除dev分支
#以下两条为初次创建仓库时使用
git remote add origin https://github.com/Jin-Tianyi/springcloudproject.git  #添加远程仓库
git push --set-upstream origin master   #推送至远程master 分支
#已创建远程master分支时
git push origin master  #推送至远程master 分支
git push -u origin master -f #推送强制覆盖已有的分支

#新建分支
git branch eureka 
git checkout eureka #新建本地分支eureka
git push origin eureka  #新建远程分支并推送至eureka
git push origin --delete [branch_name] #删除分支 删除后需要commit push

```
##### 四、本地代码关联远程仓库
```
git init #初始化仓库
git remote add origin https://github.com/Jix/xxxx.git  #添加远程仓库
git add .
git commit -m 'first commit'
git push --set-upstream origin master   #推送至远程master 分支
```
##### 五、远程仓库拉取到本地
```
git clone https://github.com/Jix/xxxx.git 
```



##### 操作记录
```$git
git log #查看操作记录
#--oneline 查看操作记录的简洁的版本
#--reverse 逆向显示所有日志
#--author= 张三 查看该操作用户的记录
```