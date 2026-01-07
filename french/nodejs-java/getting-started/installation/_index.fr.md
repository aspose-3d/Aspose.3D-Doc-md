---
title: Installation
type: docs
weight: 40
url: /fr/nodejs-java/installation/
---
##  **Exigences système**

Tout d'abord, vous devez vérifier et confirmer que les spécifications de la machine répondent au [Exigences du système](/3d/fr/nodejs-java/system-requirements/).

##  **Installation de Aspose.3D for Node.js via Java**
`npm` est le moyen le plus simple de télécharger et d'installer [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

Pour installer Aspose.3D, exécutez cette commande: npm install aspose.3d

##  **Utilisation de Aspose.3D for Node.js via Java**

Une fois l'installation du module terminée, vous pouvez utiliser Aspose.3D à partir de votre code Node.js de cette façon:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.3d");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

