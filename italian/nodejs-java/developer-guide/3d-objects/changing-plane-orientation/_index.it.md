---
title: Cambiamento dell'orientamento aereo
type: docs
weight: 70
url: /it/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java consente di modificare l'orientamento di una scena. Per cambiare l'orientamento, i metodi getUp() e setUp() vengono introdotti in Plane Class.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 23.12 o maggiore.

{{% /alert %}} 

#  **Cambiamento dell'orientamento aereo**
Aspose.3D for Node.js via Java consente di modificare l'orientamento di una scena. Per modificare l'orientamento, i metodi `getUp()` e `setUp()` vengono introdotti nella classe `Plane`. Il seguente frammento di codice mostra come modificare l'orientamento dell'aereo:

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
