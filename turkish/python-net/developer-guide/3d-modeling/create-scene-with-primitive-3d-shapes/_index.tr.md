---
title: İlkel 3D şekilleri ile sahne oluşturun
type: docs
weight: 10
url: /tr/python-net/create-scene-with-primitive-3d-shapes/
description: Using Aspose.3D for Python via .NET, developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.

{{% /alert %}}
##  **İlkel 3D şekillerinden sahne oluşturun**
Modelleme, saf yaratma ve Aspose sürecidir. 3D API, primitive 3D şekilleriyle bir sahne oluşturmayı destekler.
###  **Programming ample ample**
Bu kod örneği, İlkel 3D şekilleri ile bir sahne oluşturur ve FBX dosyasında tasarruf sağlar.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
