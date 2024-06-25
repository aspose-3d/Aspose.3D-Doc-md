---
title: Installation
type: docs
weight: 40
url: /sv/nodejs-java/installation/
---
##  **Systemkrav**

Först måste du kontrollera och bekräfta att maskinens specifikationer uppfyller [Systemkrav](/3d/sv/nodejs-java/system-requirements/).

##  **Installerar Aspose.3D for Node.js via Javae**
`npm` är det enklaste sättet att ladda ner och installera [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

För att installera Aspose.3D, kör det här kommandot: npm installera aspose.3d

##  **Använder Aspose.3D for Node.js via Javae**

När du har installerat modulen, kan du använda Aspose.3D från din Node.js-kod på det här sättet:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.threed");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

