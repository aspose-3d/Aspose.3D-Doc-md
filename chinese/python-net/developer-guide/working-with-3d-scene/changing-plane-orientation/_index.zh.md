---
title: 改变平面方向
type: docs
weight: 40
url: /zh/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET 允许更改场景的方向。为了改变方向，在Plane类中引入了向上向量属性。
---
#  **改变平面方向**
Aspose.3D for Python via .NET 允许更改场景的方向。为了改变方向，在 `Plane` 类中引入了 `up` 向量属性。以下代码片段显示了如何更改平面的方向:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Plane
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the data directory
dataDir = "data-dir"
#  Initialize scene object
scene = Scene()
plane = Plane()
plane.up = Vector3(1, 1, 3)
#  Set Vector
scene.root_node.create_child_node(plane)
# This will generate a plane that has customized orientation
scene.save(dataDir + "ChangePlaneOrientation.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
