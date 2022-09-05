# Git学习记录

使用命令

>ssh-keygen -t rsa -C "youremail@example.com"

生成对应的SSH Key，之后从.ssh文件夹下的id_rsa.pub文件复制key到github或者gitee等

## git config

- --system 说明设置是对整个系统有效的，包括系统内的所有用户
- --global 说明设置是对当前用户有效，如若切换了用户则无效
- --list或-l 查看当前已有的配置
- 也可查看某一个变量的值，只需要后面跟下面的任意值
- -e 对当前仓库编辑git配置文件
- -e --global 对用户下所有仓库编辑git配置文件

- user.name "Name" 用于设置个人的用户名
- user.email Email 用于设置个人的邮箱
- core.editor Editor 用于设置git默认的编辑器
- merge.tool Tool 用于差异分析的默认工具

## git add

添加文件

- git add * 可以指定后缀名
- git add < fileName >

## git reset

- git reset HEAD 使用HEAD指向的分支下的目录树替换index暂存区的目录树，不影响工作区

## git rm

- git rm --cached < fileName > / * 删除暂存区的文件，不影响工作区

## git checkout

- git checkout . 使用暂存区的文件全部替换工作区文件
- git checkout -- < fileName > 使用暂存区指定文件替换工作区文件
- git checkout HEAD . 使用HEAD指向的分支下的全部文件替换暂存区和工作区的全部文件
- git checkout HEAD < fileName > 使用HEAD指向分支的指定文件替换暂存区的工作区的文件
- git checkout < branchName > 切换到分支
- git checkout -b < branchName > 新建一个分支并切换

## git init

- git init 初始化为git仓库，这会在此目录下生成一个.git目录
- git init < repoName > 指定目录初始化

## git commit

- git commit -m "描述" 提交文件到暂存区并进行描述，在Linux系统和gitbash中'，在Windows系统中"

## git clone

- git clone < repo > 从本地或远程仓库克隆副本到当前目录
- git clone < repo > < directory > 指定要克隆到的目录位置

在命令末尾加上新名称可自定义克隆文件的目录名

## git status

查看仓库当前的状态，显示有变更的文件

## git diff

比较文件的不同，暂存区和工作区

## git mv

移动或重命名工作区文件

## git log

查看历史提交记录

- --oneline 简洁
- --graph 拓扑图
- --reverse 逆向显示
- --author=< userName > 显示指定用户的
- --decorate 查看标签

## git blame < fileName >

以列表形式查看指定文件的历史修改记录

## git remote

查看当前配置的远程仓库

- git remote add < repoName > < repo > 添加远程仓库
- git remote -v 看到这些远程仓库的实际链接地址
- git remote rm < repoName > 删除远程仓库

## git fetch

从远程获取分支

- git fetch < repoName > 获取指定远程仓库的代码

## git pull

下载远程代码并合并

## git push

上传到远程仓库并合并

- git push < repoName > < branchName > 推送指定分支到指定远程仓库

## git branch

- git branch < branchName > 创建一个新的分支
- git branch -d < branchName > 删除分支
- git branch 列出本地分支

## git merge

从远程仓库分支合并到本地分支

- git merge < branchName > 合并其他分支到当前指定分支

## git tag

查看所有标签

追加添加标签只需要在末尾添加提交ID

- -a 打标签时添加注释
