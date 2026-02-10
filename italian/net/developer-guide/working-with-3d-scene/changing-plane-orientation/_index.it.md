---
title: Cambiamento dell'orientamento aereo
type: docs
weight: 40
url: /it/net/changing-plane-orientation/
description: Aspose.3D for .NET consente di modificare l'orientamento di una scena. Per modificare l'orientamento, la proprietà vettore Up viene introdotta in Classe aereo.
---
##  **Cambiamento dell'orientamento aereo**
Aspose.3D for .NET consente di modificare l'orientamento di una scena. Per modificare l'orientamento, la proprietà vettoriale `Up` viene introdotta nella classe `Plane`. Il seguente frammento di codice mostra come modificare l'orientamento dell'aereo:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
