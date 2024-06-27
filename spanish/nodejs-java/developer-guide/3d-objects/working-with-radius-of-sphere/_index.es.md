---
title: Trabajando con Radio de Esfera
type: docs
weight: 50
url: /es/nodejs-java/working-with-radius-of-sphere/
description: Usando Aspose.3D for Node.js via Java, puede establecer de obtener el radio de una esfera.
---
##  **Trabajando con Radio de Esfera**
Usando Aspose.3D for Node.js via Java, puede establecer de obtener el radio de una esfera. Para obtener o establecer el radio, puede usar los métodos `getRadius()` y `setRadius()` de la clase `Sphere`. El siguiente es el ejemplo de código para establecer el radio de una esfera.

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
