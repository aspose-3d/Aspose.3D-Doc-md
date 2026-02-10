---
title: Arbeta med sfärens radie
type: docs
weight: 110
url: /sv/python-net/working-with-radius-of-sphere/
description: Med Aspose.3D for Python via .NET kan du hämta radie av en sfär. För att få eller ställa in radien, kan du använda Radius egenskap av sfärklassen. Nedan följer kodprovet för att ställa in en sfärs radie.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.4 eller större.

{{% /alert %}} 
##  **Arbeta med sfärens radie**
Med Aspose.3D for Python via .NET kan du hämta radie av en sfär. För att få eller ställa in radien kan du använda `radius`-egenskapen i klassen `Sphere`. Nedan följer kodprovet för att ställa in en sfärs radie.

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
