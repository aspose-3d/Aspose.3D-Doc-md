---
title: Veränderung der Flugzeug orientierung
type: docs
weight: 70
url: /de/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java ermöglicht die Änderung der Ausrichtung einer Szene. Um die Ausrichtung zu ändern, werden die Methoden getUp() und setUp() in die Flugzeug klasse eingeführt.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 23.12 oder höher unterstützt.

{{% /alert %}} 

#  **Veränderung der Flugzeug orientierung**
Aspose.3D for Node.js via Java ermöglicht die Änderung der Ausrichtung einer Szene. Um die Ausrichtung zu ändern, werden `getUp()` und `setUp()` Methoden in `Plane` Klasse eingeführt. Das folgende Code-Snippet zeigt, wie die Ausrichtung des Flugzeugs geändert wird:

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
