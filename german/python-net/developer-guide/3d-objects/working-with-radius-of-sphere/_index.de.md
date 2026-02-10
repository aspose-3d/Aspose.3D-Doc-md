---
title: Arbeiten mit Radius of Sphere
type: docs
weight: 110
url: /de/python-net/working-with-radius-of-sphere/
description: Mit Aspose.3D for Python via .NET können Sie den Abhol radius einer Kugel festlegen. Um den Radius zu erhalten oder festzulegen, können Sie die Radius-Eigenschaft der Sphere-Klasse verwenden. Das Folgende ist das Code beispiel, um den Radius einer Kugel festzulegen.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.4 oder höher unterstützt.

{{% /alert %}} 
##  **Arbeiten Sie mit Radius of Sphere**
Mit Aspose.3D for Python via .NET können Sie den Abhol radius einer Kugel festlegen. Um einen Radius zu erhalten oder festzulegen, können Sie die Eigenschaft `radius` der Klasse `Sphere` verwenden. Das Folgende ist das Code beispiel, um den Radius einer Kugel festzulegen.

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
