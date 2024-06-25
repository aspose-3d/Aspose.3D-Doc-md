---
title: Installation
type: docs
weight: 40
url: /ru/nodejs-java/installation/
---
##  **Системные требования**

Во-первых, вы должны проверить и подтвердить, что технические характеристики машины соответствуют [Требования к системе](/3d/ru/nodejs-java/system-requirements/).

##  **Установка Aspose.3D for Node.js via Java**
`npm`-самый простой способ загрузить и установить [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

Чтобы установить Aspose.3D, выполните эту команду: npm install aspose.3d

##  **Использование Aspose.3D for Node.js via Java**

Как только вы закончите установку модуля, вы можете использовать Aspose.3D из вашего кода Node.js следующим образом:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.threed");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

