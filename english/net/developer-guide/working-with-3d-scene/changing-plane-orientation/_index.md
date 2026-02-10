---
title: Changing Plane Orientation
type: docs
weight: 40
url: /net/changing-plane-orientation/
description: Aspose.3D for .NET allows changing orientation of a scene. In order to change the orientation, Up vector property is introduced in Plane Class.
---

## **Changing Plane Orientation**
Aspose.3D for .NET allows changing orientation of a scene. In order to change the orientation, `Up` vector property is introduced in `Plane` Class. Following code snippet shows how to change the plane's orientation:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
