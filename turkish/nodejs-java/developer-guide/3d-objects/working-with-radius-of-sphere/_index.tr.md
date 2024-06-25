---
title: Sphere Radius ile orking
type: docs
weight: 50
url: /tr/nodejs-java/working-with-radius-of-sphere/
description: Using Aspose.3D for Node.js via Java, you can set of get radius of a sphere.
---
##  **Sphere Radius ile orking**
Using Aspose.3D for Node.js via Java, you can set of get radius of a sphere. In order to get or set radius, you can use `getRadius()` and `setRadius()` methods of `Sphere` class. The following is the code sample to set radius of a sphere.  

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
