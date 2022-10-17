# Shell命令

[TOC]



> ​		**其实有些命令，要用的时候查看手册就行，没必要一个一个记下来，但是这些是常用的，得熟悉掌握。**

## 目录信息查看——ls 

> ​		ls -a 显示目录所有文件及文件夹，包括隐藏文件，比如以.开头的，一般在我们创建新文件夹或者删除文件夹的时候，都需要看一眼。

```shell
ls
# 查看某个文件
ls test1/
# 查看所有的
ls -a
# 详细地查看
ls -l
# 详细地查看所有的
ls -al

```

![image-20221016220330907](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016220330907.png)

## 目录切换——cd 

> ​		这个和dos以及git都是一样的，就不过多介绍了。

## 当前路径显示——pwd

> ​		就是简单的查看当前路径

```shell
# 根目录
cd /
# 返回上一级
cd ../
```

![image-20221016215154224](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016215154224.png)

## 系统信息查看——uname

> ​		就是查看我们目前是哪个系统。

```shell
#查看
uname
# 详细地查看
uname -a
```

![image-20221016215324065](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016215324065.png)

## 清理屏幕——clear

> ​		这个真的会把终端上的内容全部清除，我就不展示了。

## 显示文件内容——cat

> ​		就是显示内容，比较简单。

![image-20221016215635689](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016215635689.png)

## 切换用户身份——sudo

> ​		这个主要用来切换身份，因为我们有些操作需要root权限来运行，就像windows里面的管理员权限一样。

```shell
# 以root用户运行，非常不建议
sudo su
```

## 切换用户——su

> ​		一般配合sudo来使用，目前功能还不熟，等我去学习一下。

## 创建文件——touch

> ​		这个是新建文件，不是新建文件夹哈。

```shell
touch a.txt
```

![image-20221016221944370](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016221944370.png)

## 文件拷贝——cp

> ​		这个拷贝，比较简单。

```shell
cp a.txt b.txt
```

![image-20221016222144116](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016222144116.png)

## 删除——rm

> ​		删除

```shell
rm a.txt
# 删文件夹
rm test/ -rf
# 删库(不建议使用)
rm /* -rf
```

![image-20221016222327299](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016222327299.png)

## 创建文件夹——mkdir

> ​		建立一个文件夹，与touch有不同的。

```shell
mkdir test
```

![image-20221016222348717](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016222348717.png)

## 目录删除——rmdir

> ​		跟上面那个相反，删除文件夹。

```shell
rmdir test/
```

![image-20221016222841262](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016222841262.png)

## 移动文件——mv

> ​		其实除了移动文件的功能，这个还能用来文件改名。

```shell
# 改名
mv b.txt a.txt
# 移动
mv a.c test1/
```

## 显示网络配置信息——ifconfig

> ​		显示一下网络信息，可以打开和关闭网卡，就是使用前可能要下载一下。以及修改IP地址，在此就不做展示了。

```shell
ifconfig
# 打开网卡
sudo ifconfig eth33 up
# 关闭网卡
sudo ifconfig eth33 down
```

![image-20221016233636120](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221016233636120.png)

## 重启——reboot

> ​		不展示，就重启命令。

```shell
reboot
```



## 关机——poweroff

> ​		同上，关机命令。

```shell
poweroff
```



## 系统帮助——man

> ​		这个用来查看帮助，可以用来看一些详细信息。

```shell
man printf
```

![image-20221017184735832](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017184735832.png)

## 数据同步写入磁盘——sync

> ​		这个命令主要用来确保我们的文本什么的写入到了磁盘里面。

```shell
sync
```

![image-20221017185248067](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017185248067.png)

## 查找文件——find

> ​		这个主要用来查找我们的文件放在哪，当然，还有很多操作，就不一一介绍了。	

```shell
find -name a.c
```

![image-20221017185750169](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017185750169.png)

## 查找内容——grep

> ​		这个主要用来查找内容，相当于我们windows下的查找操作。

```shell
grep -nr "Ubuntu"
```

![image-20221017194053723](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017194053723.png)

## 文件夹大小查看——du

> ​		这个命令用来查看文件的大小，加上-sh就是以我们人能看懂的放松去显示。

```shell
du test1/
# 以人类可读
du test1/ -sh
```

![image-20221017194409120](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017194409120.png)

## 磁盘空间检查——df

> ​		这个就是用来查看我们磁盘的使用情况。
>

```shell
df
```

![image-20221017194759900](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017194759900.png)

## 打开文件——gedit

> ​		这个就是用来打开我们的文件,之后就能对文件进行编辑了。

```shell
gedit a.c
```

![image-20221017195139455](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017195139455.png)

## 当前的系统进程查看——ps

> ​		这个用来查看系统进程，在嵌入式开发比较常用。

![image-20221017204851857](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017204851857.png)

## 进程实时运行状态查看——top

> ​		有点像是windows下的资源管理器，能实时查看运行状态。

```shell
top
```

![image-20221017205302820](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017205302820.png)

## 文件类型查看——file

> ​	就是用来查看文件类型，在嵌入式用的蛮多。

```shell
file a.c
```

![image-20221017224339164](C:\Users\ye'gao'rui\AppData\Roaming\Typora\typora-user-images\image-20221017224339164.png)
