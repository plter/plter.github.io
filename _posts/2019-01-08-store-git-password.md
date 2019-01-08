---
layout: post
title:  "记录git的用户名和密码"
date:   2019-01-08 14:07:00 +0800
categories: tools
---  

### 永久记住密码

```bash
git config --global credential.helper store
```

### 只记住当前库的密码 

```bash
git config credential.helper store
```  

### 编辑.git/config 文件记住密码  

也可以通过编辑 .git/config 文件以记住密码，只需要在该文件中添加如下代码即可。 

```text
[credential]
	helper = store
```