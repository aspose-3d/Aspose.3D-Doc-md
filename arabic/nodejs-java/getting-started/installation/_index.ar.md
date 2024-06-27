---
title: Installation
type: docs
weight: 40
url: /ar/nodejs-java/installation/
---
##  **متطلبات النظام**

أولاً ، يجب عليك التحقق والتأكد من أن مواصفات الجهاز تفي بسعر [متطلبات النظام](/3d/ar/nodejs-java/system-requirements/).

##  **تثبيت Aspose.3D for Node.js via Java**
`npm` هو أسهل طريقة لتنزيل وتثبيت [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

لتثبيت Aspose.3D ، قم بتشغيل هذا الأمر: npm install aspose.3d

##  **Using Aspose.3D for Node.js via Java**

بمجرد الانتهاء من تثبيت الوحدة النمطية ، يمكنك استخدام Aspose.3D من رمز Node.js بهذه الطريقة:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.threed");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

