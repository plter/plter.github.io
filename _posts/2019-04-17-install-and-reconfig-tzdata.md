---
layout: post
title:  "安装及重新配置tzdata"
date:   2019-04-17 14:10:00 +0800
categories: tools
---  

* 在Linux Debian系统中安装时间相关工具的命令如下所示  
```shell
apt install tzdata
```  
在安装过程中会出现选择时区的相关配置提示  
* 如果想重新配置时间选择，则使用下面所示的命令  
```shell
dpkg-reconfigure tzdata
```
