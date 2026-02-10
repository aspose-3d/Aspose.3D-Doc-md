---
title: Working with Radius of Sphere
type: docs
weight: 110
url: /net/working-with-radius-of-sphere/
description: Using Aspose.3D for .NET, you can set of get radius of a sphere. In order to get or set radius, you can use Radius property of Sphere class. The following is the code sample to set radius of a sphere.  
---

{{% alert color="primary" %}} 

This feature is supported by version 19.4 or greater.

{{% /alert %}} 
## **Work with Radius of Sphere**
Using Aspose.3D for .NET, you can set of get radius of a sphere. In order to get or set radius, you can use `Radius` property of `Sphere` class. The following is the code sample to set radius of a sphere.  

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
