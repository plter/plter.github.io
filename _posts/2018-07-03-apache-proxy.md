---
layout: post
title:  "Apache代理设置"
date:   2018-07-03 19:23:00 +0800
categories: tools
---  

如果想配置基于HTTP协议的代理，如下所示：  

```text
ProxyPass /cdb http://127.0.0.1:8080/cdb
```  

如果是Java语言所写的服务器，为了提高代理的运行效率，可使用AJP，如下所示：  
```text
ProxyPass /cdb ajp://127.0.0.1:8009/cdb
```  

如果想以Apache来处理静态文件，则可配置虚拟目录用于实现简单的负载均衡，如下所示：    
```text
Alias /cdb "/opt/apache-tomcat-9.0.10/webapps/cdb"

<Directory "/opt/apache-tomcat-9.0.10/webapps/cdb">
    Require all granted
</Directory>

ProxyPass /cdb/static !
ProxyPass /cdb ajp://127.0.0.1:8009/cdb
```
