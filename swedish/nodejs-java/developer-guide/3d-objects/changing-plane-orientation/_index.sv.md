---
title: Ändra planorientering
type: docs
weight: 70
url: /sv/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java gör det möjligt att ändra orientering av en scen. För att ändra riktningen introduceras getUp() och setUp() metoder i Plane Class.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 23.12 eller större.

{{% /alert %}} 

#  **Ändra planorientering**
Aspose.3D for Node.js via Java gör det möjligt att ändra orientering av en scen. För att ändra orienteringen introduceras `getUp()` och `setUp()` metoder i `Plane` klass. Följande kodsnutt visar hur man ändrar planets orientering:

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
