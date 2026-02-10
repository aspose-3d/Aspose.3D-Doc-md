---
title: Cambio de orientación del plano
type: docs
weight: 40
url: /es/net/changing-plane-orientation/
description: Aspose.3D for .NET permite cambiar la orientación de una escena. Para cambiar la orientación, se introduce la propiedad del vector Up en Clase de plano.
---
##  **Cambio de orientación del plano**
Aspose.3D for .NET permite cambiar la orientación de una escena. Para cambiar la orientación, se introduce la propiedad del vector `Up` en la clase `Plane`. El siguiente fragmento de código muestra cómo cambiar la orientación del plano:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
