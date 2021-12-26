# Git
## git的安装和建立GitHub连接
### 安装
Mac中App Store中直接安装git
### 创建ssh key
- 设置username和email
```
git config --global user.name "你的GitHub名字"
git config --global user.email "你的GitHub邮箱"
```
- 通过终端命令创建ssh key
```
ssh-keygen -t rsa -C "你的GitHub邮箱"
```
所有选项都回车
成功的话会生成.ssh文件夹，如果使用的是root用户的话，文件夹在/var/root/.ssh，否则文件夹在~/.ssh。
查看.ssh文件夹中的id_rsa.pub文件，复制里面的所有内容。

### github端
登录你的GitHub -> 点击右上角头像 -> Settings -> SSH and GPG keys -> New SSH key -> title 链接的标题，随便填， key中填入从.ssh/id_rsa.pub文件中复制的ssh key.

### 验证
```
ssh -T git@github.com
```
正常应该会显示
```
Hi 你的GitHub昵称! You've successfully authenticated, but GitHub does not provide shell access.
```
这样就已经配置好git和GitHub的连接了。

## git 使用
教程网站：
git-简易指南：[https://www.bootcss.com/p/git-guide/](url)
### 创建新仓库
创建新文件夹，打开，然后执行：```git init``` 创建新的仓库
### 检出仓库
执行如下命令以创建一个本地仓库的克隆版本
```
git clone /path/to/repository
```
### 添加与提交
你可以计划改动（把它们添加到缓存区），使用如下命令：
```
git add <filename>
-- 例如
git add *
```
如果要删除：
```
git rm (如果删除文件夹需要 -r) <filename>
```
这是git基本工作流程的第一步，使用如下命令以实际提交改动：
```
git commit -m "代码提交说明信息"
```
现在，你的改动已经提交到了HEAD，但是还没到你的远端仓库
### 推动改动
你的改动现在已经在本地仓库的HEAD中了。执行如下命令以将这些改动提交到远端仓库：
```
git push origin master
```
可以把master换成你想要推送的任何分支。
## git 提交时如果文件名为中文，会产生乱码：
```
new file:   "git\347\254\224\350\256\260.md"
```
需要一条命令解决：
```
git config --global core.quotepath false
```
