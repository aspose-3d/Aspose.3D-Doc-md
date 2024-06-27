---
title: Cambio de orientación del plano
type: docs
weight: 70
url: /es/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java permite cambiar la orientación de una escena. Para cambiar la orientación, se introducen los métodos getUp() y setUp() en Plane Class.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 23,12 o superior.

{{% /alert %}} 

#  **Cambio de orientación del plano**
Aspose.3D for Node.js via Java permite cambiar la orientación de una escena. Para cambiar la orientación, los métodos `getUp()` y `setUp()` se introducen en `Plane` Class. El siguiente fragmento de código muestra cómo cambiar la orientación del plano:

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

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
