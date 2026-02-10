---
title: Create Scene with Primitive 3D Shapes
type: docs
weight: 10
url: /net/create-scene-with-primitive-3d-shapes/
description: Using Aspose.3D for .NET, developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.

{{% /alert %}}
## **Build Scene from Primitive 3D Shapes**
Modeling is the process of pure creation and Aspose.3D API supports creating a scene with primitive 3D shapes.
### **Programming Sample**
This code example creates a scene with primitive 3D shapes and save in the FBX file.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
