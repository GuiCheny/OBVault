
## L简介

  

Linux是一套免费使用和自由传播的类Unix操作系统，是一个基于POSIX和UNIX的多用户、多任务、支持多线程和多CPU的操作系统。Linux能运行主要的UNIX工具软件、应用程序和网络协议。它支持32位和64位硬件。Linux继承了Unix以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。
## 常用命令

### linux

- 系统信息:`lsb_release -a` or `cat /etc/os-release`
- 查看当前桌面环境:echo $XDG_CURRENT_DESKTOP
- 查看已经安装的桌面环境软件包:
- 查看默认的显示器管理器配置文件:`cat /etc/X11/default-display-manager`
- 查看内存使用情况:`free`
- 查看硬盘使用情况:`df`

### 文件管理

- 回到根目录:`cd /`
- 返回上一级:`cd ..`
- 创建文件夹:`mkdir folder_name`
- 查看当前目录中的文件和子目录:`ls`
- 以长格式列出文件和子目录:`ls -l`
- 列出当前目录中的所有文件: `ls -a`
- 列出当前目录中的指定后缀文件: `ls *.sh`
- 列出当前目录中的所有文件夹:`ls -d */`
- 删除文件夹 rm -r

### 软件安装

- 更新软件包列表：`sudo apt-get update`
- 安装软件: sudo apt-get install xx
- 创建文件夹 wget bash rm 
- 查找软件: which xx
- 
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

### 其他命令

#### wget——下载网络文件

wget is "web get"

语法:`wget(选项)(参数)`

选项

```

-a<日志文件>：在指定的日志文件中记录资料的执行过程；

-A<后缀名>：指定要下载文件的后缀名，多个后缀名之间使用逗号进行分隔；

-b：进行后台的方式运行wget；

-B<连接地址>：设置参考的连接地址的基地地址；

-c：继续执行上次终端的任务；

-C<标志>：设置服务器数据块功能标志on为激活，off为关闭，默认值为on；

-d：调试模式运行指令；

-D<域名列表>：设置顺着的域名列表，域名之间用“，”分隔；

-e<指令>：作为文件“.wgetrc”中的一部分执行指定的指令；

-h：显示指令帮助信息；

-i<文件>：从指定文件获取要下载的URL地址；

-l<目录列表>：设置顺着的目录列表，多个目录用“，”分隔；

-L：仅顺着关联的连接；

-r：递归下载方式；

-nc：文件存在时，下载文件不覆盖原有文件；

-nv：下载时只显示更新和出错信息，不显示指令的详细执行过程；

-q：不显示指令执行过程；

-nh：不查询主机名称；

-v：显示详细执行过程；

-V：显示版本信息；

--passive-ftp：使用被动模式PASV连接FTP服务器；

--follow-ftp：从HTML文件中下载FTP连接文件。

```

参数

```

URL：下载指定的URL地址

```