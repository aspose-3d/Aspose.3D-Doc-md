---
title: Working مع Radius من Sphere
type: docs
weight: 50
url: /ar/nodejs-java/working-with-radius-of-sphere/
description: باستخدام Aspose.3D for Node.js via Java ، يمكنك تعيين الحصول على نصف قطر كروي.
---
##  **Working مع Radius من Sphere**
باستخدام Aspose.3D for Node.js via Java ، يمكنك تعيين الحصول على نصف قطر كروي. للحصول على نصف قطر أو ضبطه ، يمكنك استخدام طرق `getRadius()` و `setRadius()` لفئة `Sphere`. فيما يلي عينة الكود لتعيين نصف قطر كروي.

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
