---
title: İlkel 3D şekilleri ile sahne oluşturun
type: docs
weight: 10
url: /tr/net/create-scene-with-primitive-3d-shapes/
description: Using Aspose.3D for .NET, developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.

{{% /alert %}}
##  **İlkel 3D şekillerinden sahne oluşturun**
Modelleme, saf yaratma ve Aspose sürecidir. 3D API, primitive 3D şekilleriyle bir sahne oluşturmayı destekler.
###  **Programming ample ample**
Bu kod örneği, İlkel 3D şekilleri ile bir sahne oluşturur ve FBX dosyasında tasarruf sağlar.

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
