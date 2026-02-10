---
title: Create Scene with Primitive 3D Shapes
type: docs
weight: 10
url: /python-net/create-scene-with-primitive-3d-shapes/
description: Using Aspose.3D for Python via .NET, developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.
---

{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), developers can define a scene with primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.

{{% /alert %}}
## **Build Scene from Primitive 3D Shapes**
Modeling is the process of pure creation and Aspose.3D API supports creating a scene with primitive 3D shapes.
### **Programming Sample**
This code example creates a scene with primitive 3D shapes and save in the FBX file.

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
