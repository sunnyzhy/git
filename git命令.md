# push to github
```
$ git add -f dir (提交打开的目录下面的所有文件)

$ git add --all (提交打开的目录下面的所有目录和文件)

$ git add filename (提交文件)

$ git add "filename" (提交带有特殊字符的文件)

$ git commit -m "备注" (提交新增的文件)

$ git commit -a -m "备注" (提交内容有变化的文件)

$ git push
```


# clone from github
```
$ cd dir

$ git clone giturl
```


# 从服务器上更新到本地
```
$ git checkout -- file or dir
```

# 将服务器代码更新到本地
```
$ git pull
```

# 强制更新到服务器
```
$ git push --force
```

# 创建远程仓库
1. 检测SSH keys，若已经存在key，就直接进入第4步
```
$ cd ~/.ssh
```

2. 备份原来的SSH keys并删除
```
$ mkdir key_backup

$ cp id_rsa* key_backup

$ rm id_rsa*
```

3. 创建SSH Key
```
$ ssh-keygen -t rsa -C "iamaant100@163.com" 
使用默认设置，一路回车即可；
根据提示的"saved in 路径"，在该路径下会生成.ssh的文件夹，里面有id_rsa和id_rsa.pub两个文件；
登陆https://github.com/settings/ssh；
点击New SSH key，把id_rsa.pub文件的内容直接复制到Key文本框中，Title内容自定义，保存。
```

4. 测试是否能够正确链接到github
```
$ ssh -T git@github.com
显示出下列信息表示连接成功
Hi sunnyzhy! You've successfully authenticated, but GitHub does not provide shell access.
```

5. 创建本地仓库
```
$ mkdir testgit

$ cd testgit

$ git init

$ touch README --创建README文件

$ echo test > 1.txt

$ git add --all

$ git commit -m "add test txt file"
```

6. 在github上创建一个新的仓库testgit

7. 将本地仓库推送到远程仓库
```
$ git remote add origin https://github.com/sunnyzhy/testgit.git

$ git push -u origin master
```

# 还原本地未提交的代码
```
$ git rm --cached

$ git checkout *
```
