---
title: Arbeiten mit Radius of Sphere
type: docs
weight: 50
url: /de/nodejs-java/working-with-radius-of-sphere/
description: Mit Aspose.3D for Node.js via Java können Sie den Abhol radius einer Kugel festlegen.
---
##  **Arbeiten mit Radius of Sphere**
Mit Aspose.3D for Node.js via Java können Sie den Abhol radius einer Kugel festlegen. Um Radius zu erhalten oder festzulegen, können Sie `getRadius()` und `setRadius()` Methoden der `Sphere` Klasse verwenden. Das Folgende ist das Code beispiel, um den Radius einer Kugel festzulegen.

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
