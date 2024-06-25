---
title: Lavorare con il raggio della sfera
type: docs
weight: 50
url: /it/nodejs-java/working-with-radius-of-sphere/
description: Utilizzando Aspose.3D for Node.js via Java, è possibile impostare il raggio di ottenere di una sfera.
---
##  **Lavorare con il raggio della sfera**
Utilizzando Aspose.3D for Node.js via Java, è possibile impostare il raggio di ottenere di una sfera. Per ottenere o impostare il raggio, puoi utilizzare i metodi `getRadius()` e `setRadius()` della classe `Sphere`. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

 // initialize a scene
var scene = new aspose.threed.Scene();

// initialize a Sphere
var sphere=new aspose.threed.Sphere();

 // set radius
sphere.setRadius(10);

// add sphere to the scene
scene.getRootNode().createChildNode(sphere);

// save scene
scene.save("sphere.obj");

{{< /highlight >}}
