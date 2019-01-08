---
layout: post
title:  "IframeBridge使用方式"
date:   2018-07-30 14:38:00 +0800
categories: html5
---  

IframeBridge项目开源地址：
[https://github.com/plter/IframeBridge](https://github.com/plter/IframeBridge)  

IframeBridge 用于在同一个页面中的不同框架之间跨域通信。  

比如主页面与嵌入的页面之间通信，方式如下：  

index.html 文件内容如下  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script src="../../lib/iframebridge.js"></script>
</head>
<body>
<script>
    (function () {
        let frame = document.createElement("iframe");
        document.body.appendChild(frame);

        frame.onload = function () {
            let bridge = IframeBridge.create(frame.contentWindow);
            bridge.hello("Hello iframe");
        };
        frame.src = "content.html";
    })();
</script>
</body>
</html>
```

对应的 content.html 内容如下  

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="../../lib/iframebridge.js"></script>
</head>
<body>
<script>
    (function () {
        let bridge = IframeBridge.create(window);
        bridge.hello = function (name) {
            console.log(name);
        }
    })();
</script>
</body>
</html>
```

