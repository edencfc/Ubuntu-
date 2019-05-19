



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

![识别盘符](https://github.com/edencfc/Ubuntu-Study/blob/master/2019-05-19%2020-02-15.png)
## /etc/fstab修改
`vim fstab`打开文件，参考已有的盘符将需要挂载的硬盘信息添加进去



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAxOTI2MjU4NywtNTczNzg1MTIxXX0=
-->