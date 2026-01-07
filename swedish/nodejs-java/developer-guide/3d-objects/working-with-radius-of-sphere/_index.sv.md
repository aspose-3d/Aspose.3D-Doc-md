---
title: Arbeta med sfärens radie
type: docs
weight: 50
url: /sv/nodejs-java/working-with-radius-of-sphere/
description: Med Aspose.3D for Node.js via Java kan du hämta radie av en sfär.
---
##  **Arbeta med sfärens radie**
Med Aspose.3D for Node.js via Java kan du hämta radie av en sfär. För att få fram eller ställa in radie kan du använda `getRadius()` och `setRadius()`-metoder i klassen `Sphere`. Nedan följer kodprovet för att ställa in en sfärs radie.

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
