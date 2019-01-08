---
layout: post
title:  "配置SSH服务器以使用证书登陆"
date:   2018-08-23 14:38:00 +0800
categories: tools
---  

下面以192.168.1.104上的主机为服务器来演示  

1. 在服务器端使用 `ssh-keygen` 命令生成密钥对，将在 `~/.ssh` 目录下生成id_rsa和id_rsa.pub两个文件，其中id_rsa是私钥，id_rsa.pub是公钥。
2. 通过命令 `cat ~/.ssh/id_rsa.pub >> ～/.ssh/authorized_keys` 将公钥添加到授权文件中
3. 将 `id_rsa` 文件下载到本地，通过命令 `ssh -i ./id_rsa root@192.168.1.104` 进行登陆 

