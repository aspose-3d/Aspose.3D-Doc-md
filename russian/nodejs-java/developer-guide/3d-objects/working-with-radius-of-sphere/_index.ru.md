---
title: Работа с радиусом сферы
type: docs
weight: 50
url: /ru/nodejs-java/working-with-radius-of-sphere/
description: Используя Aspose.3D for Node.js via Java, вы можете установить радиус получения сферы.
---
##  **Работа с радиусом сферы**
Используя Aspose.3D for Node.js via Java, вы можете установить радиус получения сферы. Чтобы получить или установить радиус, вы можете использовать методы `getRadius()` и `setRadius()` класса `Sphere`. Ниже приведен пример кода для установки радиуса сферы.

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
