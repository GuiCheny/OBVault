# Linux
## Linux常用命令
- 系统信息:`lsb_release -a` or `cat /etc/os-release`
- 查看当前桌面环境:echo $XDG_CURRENT_DESKTOP
- 查看已经安装的桌面环境软件包:
- 查看默认的显示器管理器配置文件:`cat /etc/X11/default-display-manager`
- 查看内存使用情况:`free`
- 查看硬盘使用情况:`df`
## 文件管理
- 回到根目录:`cd /`
- 返回上一级:`cd ..`
- 创建文件夹:`mkdir folder_name`
- 查看当前目录中的文件和子目录:`ls`
- 以长格式列出文件和子目录:`ls -l`
- 列出当前目录中的所有文件: `ls -a`
- 列出当前目录中的指定后缀文件: `ls *.sh`
- 列出当前目录中的所有文件夹:`ls -d */`
- 删除文件夹 rm -r

## 软件安装
- 更新软件包列表：`sudo apt-get update`
- 安装软件: sudo apt-get install xx
- 创建文件夹 wget bash rm 
- 查找软件: which xx
### 安装conda
1. mkdir -p ~/usr/local/miniconda3
2. cd ~/usr/local/miniconda3
3. wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
4. bash ~/usr/local/miniconda3/miniconda.sh -b -u -p ~/usr/local/miniconda3
5. rm -rf ~/usr/local/miniconda3/miniconda.sh
6. vim ~/.bashrc
7. 末尾添加export PATH="$PATH:/your/new/directory"
8. 改动生效:source ~/.bashrc

## 软件卸载
- 使用包管理器卸载 apt remove --purge xxxx