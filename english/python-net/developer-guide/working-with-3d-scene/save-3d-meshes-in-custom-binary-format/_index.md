---
title: Save 3D Meshes in Custom Binary Format
type: docs
weight: 20
url: /python-net/save-3d-meshes-in-custom-binary-format/
description: Using Aspose.3D for Python via .NET API, developers can open any supported 3D file, and then write meshes in the custom binary file.
---

{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), developers can open any supported 3D file, and then write meshes in the binary file.

{{% /alert %}}
## **Load 3D File and Write Meshes in Custom Binary Format Programming Sample**
`accept` method exposed by `root_node` member in [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class allows to visit each sub node. The code snippet below allows to convert meshes only.

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Box
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load a 3D file into Aspose.3D
scene = Scene.from_file("document.fbx")
box = scene.root_node.create_child_node("box", Box()).transform
box.scale = Vector3(12, 12, 12)
box.translation = Vector3(10, 0, 0)
#  Serialize the node into binary file
with open("out" + "customData", "wb") as output:
    scene.root_node.accept(output, "3d")
{{< /highlight >}}
