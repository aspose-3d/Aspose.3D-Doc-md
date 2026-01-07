---
title: Installation
type: docs
weight: 40
url: /tr/nodejs-java/installation/
---
##  **Sistem gereksinimleri**

First, you have to check and confirm that machine’s specifications meet the [system requirements](/3d/nodejs-java/system-requirements/).

##  **Aspose.3D for Node.js via Java kurulumu**
`npm` is the easiest way to download and install [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

To install Aspose.3D, run this command: npm install aspose.3d

##  **Using Aspose.3D for Node.js via Java**

Once you finish installing the module, you can use Aspose.3D from your Node.js code this way:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.3d");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

