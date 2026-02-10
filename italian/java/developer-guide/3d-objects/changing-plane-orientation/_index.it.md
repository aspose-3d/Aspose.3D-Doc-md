---
title: Cambiamento dell'orientamento aereo
type: docs
weight: 70
url: /it/java/changing-plane-orientation/
description: Aspose.3D for Java consente di modificare l'orientamento di una scena. Per cambiare l'orientamento, i metodi getUp() e setUp() vengono introdotti in Plane Class.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.5 o maggiore.

{{% /alert %}} 
#  **Cambiamento dell'orientamento aereo**
Aspose.3D for Java consente di modificare l'orientamento di una scena. Per modificare l'orientamento, i metodi `getUp()` e `setUp()` vengono introdotti nella classe `Plane`. Il seguente frammento di codice mostra come modificare l'orientamento dell'aereo:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
