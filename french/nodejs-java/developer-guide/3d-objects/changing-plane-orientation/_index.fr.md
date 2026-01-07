---
title: Changer l'orientation de l'avion
type: docs
weight: 70
url: /fr/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java permet de changer l'orientation d'une scène. Afin de changer l'orientation, les méthodes getUp() et setUp() sont introduites dans Plane Class.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 23.12 ou supérieure.

{{% /alert %}} 

#  **Changer l'orientation de l'avion**
Aspose.3D for Node.js via Java permet de changer l'orientation d'une scène. Afin de changer l'orientation, les méthodes `getUp()` et `setUp()` sont introduites dans la classe `Plane`. L'extrait de code suivant montre comment modifier l'orientation du plan:

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
