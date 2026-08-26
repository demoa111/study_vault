
# 使用以及基础命令

```
基本命令：

ls  -a 显示隐藏文件 l详细信息   r倒序排列  R递归显示子目录内容
     S按文件大小排序  t按修改时间排列
cd + 文件名 ~主目录  ..退一级  ../../ 退两级  /根目录
touch
rm -rf
echo "数据" > 1.txt
cat
id
whoami
ip route
route -n
ss -lntp   查看开放端口
ps
ssh
kill   -9 + 进程pid
killall  +进程名称
ifconfig   
ip addr 

防火墙命令：

iptables -L 查询防火墙信息  -v 详细   -n不解析域名
iptables -t nat -L -v -n

```

# linux中的编辑

```
**vi编辑器  vim为升级版**（用法一致）
使用：vi + 文件
1、命令模式
：q     
：wq
w为保存，q为退出，带！为强制
不再编辑模式下按两次d为删除
2、输入模式
按下a或者o或者i，都可以进行编辑，esc退出编辑。

**nano编辑器**
nano + 文件  
进入可直接编辑
然后ctrl  + o  再回车表示保存
+ x为退出。
   
```

# linux的安装

```
apt install 软件名
安装前需要更新，apt update
```



# 目录结构文件

```
home    家目录
root    root用户的家目录
tmp     临时文件目录，他下面的东西，在重启后，系统自动帮我们清理
etc     所有系统级的配置文件目录
var     日志目录，缓存，数据库文件
bin     二进制程序目录  放的基础命令，什么cd ls    
sbin    系统管理命令, 放的什么关机命令， reboot  shutdown  iptebles
usr     用户安装的软件和库   像刚刚安装的wget这些都放在这里的 kali的字典也都在这里
lib     内核模块，动态链接库.so， 程序都运行基本都靠他，这里千万别去乱删除东西
opt     第三方大型的软件安装目录
boot    全是内核文件，引导和加载全都依靠他
dev     所有的硬件设备都在这里，比如硬盘    
proc    虚拟文件系统，进程信息都会放这里
sys     内核和硬件相关的虚拟文件
run     放系统启动后的动态数据，比如pid文件之类

```


# linux 权限

```
-rw-r--r-- 1 root root 3260 2025年12月25日 /etc/passwd
第一段为当前用户，第二段为当前用户组，第三段为其他用户
r为读，w为写，x为执行
r=4 w=2 x=1
777表示全放通   

chmod可更改文件权限
chown可更改文件所属

```
# linux远程连接

可通过物理机下载xshell之类的软件进行ssh远程连接到虚拟机，也可手动更改虚拟机ip地址达到ip不变的效果。