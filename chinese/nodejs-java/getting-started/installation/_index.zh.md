---
title: Installation
type: docs
weight: 40
url: /zh/nodejs-java/installation/
---
##  **系统要求**

首先，您必须检查并确认机器的规格符合 [系统要求](/3d/zh/nodejs-java/system-requirements/)。

##  **正在安装 Aspose.3D for Node.js via Java**
`npm` 是下载和安装 [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d) 的最简单方法。

若要安装 Aspose.3D，请运行以下命令: npm install aspose.3d

##  **正在使用 Aspose.3D for Node.js via Java**

一旦你完成安装模块，你可以使用 Aspose。3D 从你的Node.js代码这样:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.threed");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

