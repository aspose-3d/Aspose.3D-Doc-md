---
title: Travailler avec le rayon de la sphère
type: docs
weight: 50
url: /fr/nodejs-java/working-with-radius-of-sphere/
description: En utilisant Aspose.3D for Node.js via Java, vous pouvez définir le rayon get d'une sphère.
---
##  **Travailler avec le rayon de la sphère**
En utilisant Aspose.3D for Node.js via Java, vous pouvez définir le rayon get d'une sphère. Pour obtenir ou définir radius, vous pouvez utiliser les méthodes `getRadius()` et `setRadius()` de la classe `Sphere`. Voici l'exemple de code pour définir le rayon d'une sphère.

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

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
