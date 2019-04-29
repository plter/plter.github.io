---
layout: post
title:  "在Docker Debian容器中安装ps,top等命令"
date:   2019-04-29 11:10:00 +0800
categories: tools
---  

有些debian镜像默认没有包括进程管理相关工具，在实际使用时可能有些麻烦，如果需要也可以自己安装，使用如下命令。   

```shell
apt install procps
```