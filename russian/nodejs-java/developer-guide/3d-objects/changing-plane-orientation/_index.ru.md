---
title: Изменение ориентации плоскости
type: docs
weight: 70
url: /ru/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java позволяет изменять ориентацию сцены. Для того чтобы изменить ориентацию, методы getUp() и setUp() вводятся в класс плоскости.
---
{{% alert color="primary" %}} 

Эта функция поддерживается в версии 23,12 или выше.

{{% /alert %}} 

#  **Изменение ориентации плоскости**
Aspose.3D for Node.js via Java позволяет изменять ориентацию сцены. Чтобы изменить ориентацию, в классе `Plane` введены методы `getUp()` и `setUp()`. Следующий фрагмент кода показывает, как изменить ориентацию самолета:

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize Scene
var scene = new aspose.threed.Scene();

// Initialize Plane
var plane=new aspose.threed.Plane();

// Set Vector
plane.setUp(new aspose.threed.Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);

//This will generate a plane that has customized orientation
scene.save("ChangePlaneOrientation.obj");

{{< /highlight >}}
