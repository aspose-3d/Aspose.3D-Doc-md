---
title: 以球体半径工作
type: docs
weight: 110
url: /zh/python-net/working-with-radius-of-sphere/
description: 使用 Aspose.3D for Python via .NET，你可以设置得到一个球体的半径。为了获取或设置半径，您可以使用Sphere类的半径属性。以下是设置球体半径的代码示例。
---
{{% alert color="primary" %}} 

19.4或更高版本支持此功能。

{{% /alert %}} 
##  **以球体半径工作**
使用 Aspose.3D for Python via .NET，你可以设置得到一个球体的半径。为了获取或设置半径，您可以使用 `radius` `Sphere` 类的属性。以下是设置球体半径的代码示例。

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
sphere = Sphere()
sphere.radius = 10 .0
#  Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.root_node.create_child_node(sphere)
#  Save scene
scene.save("data-dir"  + "sphere.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
