# Emergency Mode

## 起因

起先Ubuntu系统是装在移动硬盘上通过USB连接的，由于笔记本电脑无法识别移动硬盘（可能是连接线的原因，或供电不足），将移动硬盘中的SSD拆下接入台式机的SATA接口，然而在启动时发现Ubuntu进入了Emergency Mode

## 原因分析

核对了前后盘符发现没有不一致的地方，怀疑是双系统中Windows对硬盘分区的抢夺导致的

## 处理方式

在Emergency Mode状态下：
1. 直接输入root密码
2. vi /etc/fstab
3. 将挂载NTFS分区的那几行删去
4. :wq退出
5. 不保存退出是:q!
6. 修改完成后reboot

## 另一种方式

正常进入Windows，然后重启进入Ubuntu

经确认，从Ubuntu重启进入Ubuntu是没有问题的，所以确实是抢夺硬盘加载权限导致的报错。
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM0MDQ1NjMwOCwtMTU1MDI3MTg1OSwxOT
AwMDE5Njg5LDE0ODE2NDgxNl19
-->