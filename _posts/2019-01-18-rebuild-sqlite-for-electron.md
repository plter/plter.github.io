---
layout: post
title:  "为Electron平台重新编译sqlite"
date:   2019-01-17 20:40:00 +0800
categories: electron
---  

Electron 环境与本机 Node 环境稍微有些不同，在使用npm安装有些需要编译的模块时，编译生成的文件可能与Electron内置的Node不环境不匹配，从而导致无法运行，这时我们就需要使用Electron提供的工具进行重新编译。  

```shell
npm install --save-dev electron-rebuild
./node_modules/.bin/electron-rebuild
```