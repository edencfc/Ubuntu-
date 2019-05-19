



> Written with [StackEdit](https://stackedit.io/).

# 开启IPV6
```bash
	sudo apt-get install miredo
	ifconfig
 ```
Ping出的结果中如果可以看到teredo就代表开启成功
   
# 安装Node.js
```bash
	sudo apt-get install nodejs
	sudo apt-get install npm
```
启用时发现npm版本太低，不能启动项目，对npm进行更新
```bash
	npm install -g npm
```
启用淘宝NPM镜像

```bash
	npm install -g cnpm --registry=https://registry.npm.taobao.org
```
# 开机自动加载NTFS硬盘

## 新建目录
准备挂载的是双系统中的E、F、G、H、I盘，首先要创建用于挂载硬盘的目录
```bash
	sudo mkdir /mnt/e
	sudo mkdir /mnt/f
	sudo mkdir /mnt/g
	sudo mkdir /mnt/h
	sudo mkdir /mnt/i
```
## 识别盘符
找到Ubuntu中文件盘名称和Windows盘符的对应，记录下来

![file](https://raw.githubusercontent.com/edencfc/Ubuntu-Study/master/20-02-15.png)

## /etc/fstab修改
首先是获得读写权限
```bash
su root
```
`vim fstab`打开文件，参考已有的盘符将需要挂载的硬盘信息添加进去
![file](https://raw.githubusercontent.com/edencfc/Ubuntu-Study/master/20-09-48.png)
如果出现`Metadata kept in Windows cache, refused to mount.`的报错，是因为双系统中Windows的硬盘并未彻底关闭，原因在Windows的快速启动功能，一种办法是关闭系统重启，进入Windows登录界面（不要登录）直接重启，再F12进入Ubuntu，重新修改fstab文件。

## 挂载硬盘
```bash
	sudo mount -a
```
这样重启后E-I的NTFS分区都会自动加载了，确认以下：
```bash
	cd ../../mnt
	ls
```
看到e～i的目录直接进入，就能看到分区文件了
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjUxOTE0NTk4LDEzMzYzODE2NjMsLTU3Mz
c4NTEyMV19
-->