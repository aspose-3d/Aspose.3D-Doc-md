---
title: Trabajando con Radio de Esfera
type: docs
weight: 110
url: /es/python-net/working-with-radius-of-sphere/
description: Usando Aspose.3D for Python via .NET, puede establecer de obtener el radio de una esfera. Para obtener o establecer el radio, puede usar la propiedad Radius de la clase Sphere. El siguiente es el ejemplo de código para establecer el radio de una esfera.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,4 o superior.

{{% /alert %}} 
##  **Trabajar con Radio de la Esfera**
Usando Aspose.3D for Python via .NET, puede establecer de obtener el radio de una esfera. Para obtener o establecer el radio, puede usar la propiedad `radius` de la clase `Sphere`. El siguiente es el ejemplo de código para establecer el radio de una esfera.

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
