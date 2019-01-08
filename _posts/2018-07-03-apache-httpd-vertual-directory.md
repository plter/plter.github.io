---
layout: post
title:  "Apache虚拟目录配置"
date:   2018-07-03 19:17:00 +0800
categories: tools
---  


```text
Alias /cdb "/opt/apache-tomcat-9.0.10/webapps/cdb"

<Directory "/opt/apache-tomcat-9.0.10/webapps/cdb">
    Require all granted
</Directory>
```