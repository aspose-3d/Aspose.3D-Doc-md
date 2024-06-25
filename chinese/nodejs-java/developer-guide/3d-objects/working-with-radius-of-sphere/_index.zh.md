---
title: 以球体半径工作
type: docs
weight: 50
url: /zh/nodejs-java/working-with-radius-of-sphere/
description: 使用 Aspose.3D for Node.js via Java，你可以设置得到一个球体的半径。
---
##  **以球体半径工作**
使用 Aspose.3D for Node.js via Java，你可以设置得到一个球体的半径。为了获取或设置半径，您可以使用 `Sphere` 类的 `getRadius()` 和 `setRadius()` 方法。以下是设置球体半径的代码示例。

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
