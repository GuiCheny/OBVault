# Use git for github

### 1. 安装Git

**Linux：**
1. 更新系统包列表:`sudo apt-get update`。
2. 安装git:`sudo apt install git`。
3. 查看git版本:`git --version`。
  
**Windows:** git官网: <https://git-scm.com/>

### 2. 配置全局git信息

1. 绑定Github账户:
   - `git config --global user.email "email@example.com" // Github账号的注册邮箱.`
   - `git config --global user.name "name" // Github账号name.`
2. 查看配置信息:`git config --list`。

### 2. 配置SSH密钥

1. 生成ssh密钥:`ssh-keygen -t rsa -C "email@example.com" // Github的注册邮箱`。然后回车..回车  
2. 查看并复制公钥:`cat ~/.ssh/id_rsa.pub`。全部复制。
3. 配置Github公钥:Github->"Settings"->"SSH and GPG keys"->"New SSH key"。

### 3. 创建Github Repository

### 4. 创建本地文件夹

可以直接`git clone 远程仓库ssh地址`。这样的话，本地会**直接连接好远程仓库**。

### 5. Git操作

1. Git初始化:`git init`。
2. 重新命名本地分支为主分支名称:`git branch -m main`。
3. 关联远程仓库:`git remote add origin <远程仓库ssh地址>`
4. 添加文件到暂存区:`git add <文件>`，--all或.代表所有更改的文件。
5. 提交文件到本地仓库:`git commit -m "注释"`。
6. 查看本地状态:`git status`。
7. 拉取远程仓库的更新:`git pull origin main`。
8. 推送到远程仓库:`git push origin main`。
