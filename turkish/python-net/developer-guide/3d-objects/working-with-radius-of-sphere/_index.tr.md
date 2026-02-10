---
title: Sphere Radius ile orking
type: docs
weight: 110
url: /tr/python-net/working-with-radius-of-sphere/
description: Using Aspose.3D for Python via .NET, you can set of get radius of a sphere. In order to get or set radius, you can use Radius property of Sphere class. The following is the code sample to set radius of a sphere.  
---
{{% alert color="primary" %}} 

This özelliği 19.4 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Sphere Radius ile Work**
Using Aspose.3D for Python via .NET, you can set of get radius of a sphere. In order to get or set radius, you can use `radius` property of `Sphere` class. The following is the code sample to set radius of a sphere.  

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
