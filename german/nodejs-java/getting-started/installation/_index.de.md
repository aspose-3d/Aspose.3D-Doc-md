---
title: Installation
type: docs
weight: 40
url: /de/nodejs-java/installation/
---
##  **Systema forderungen**

Zuerst müssen Sie überprüfen und bestätigen, dass die Spezifikationen der Maschine die [Systema forderungen](/3d/de/nodejs-java/system-requirements/) erfüllen.

##  **Installation von Aspose.3D for Node.js via Java**
`npm` ist der einfachste Weg, [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d) herunter zuladen und zu installieren.

Um Aspose.3D zu installieren, führen Sie den folgenden Befehl aus: npm install asose.3d

##  **Verwenden von Aspose.3D for Node.js via Java**

Sobald Sie mit der Installation des Moduls fertig sind, können Sie Aspose.3D aus Ihrem Node.js-Code folgender maßen verwenden:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.3d");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

