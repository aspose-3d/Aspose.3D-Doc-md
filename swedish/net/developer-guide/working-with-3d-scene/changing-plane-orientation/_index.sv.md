---
title: Ändra planorientering
type: docs
weight: 40
url: /sv/net/changing-plane-orientation/
description: Aspose.3D for .NET tillåter ändrad orientering av en scen. För att ändra orienteringen introduceras upp vektoregenskapen i Plane Class.
---
##  **Ändra planorientering**
Aspose.3D for .NET tillåter ändrad orientering av en scen. För att ändra orienteringen, introduceras `Up` vektoregenskapen i `Plane` klass. Följande kodsnutt visar hur man ändrar planets orientering:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
