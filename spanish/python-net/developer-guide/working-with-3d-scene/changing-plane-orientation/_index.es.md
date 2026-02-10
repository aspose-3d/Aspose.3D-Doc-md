---
title: Cambio de orientación del plano
type: docs
weight: 40
url: /es/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET permite cambiar la orientación de una escena. Para cambiar la orientación, se introduce la propiedad del vector Up en Clase de plano.
---
#  **Cambio de orientación del plano**
Aspose.3D for Python via .NET permite cambiar la orientación de una escena. Para cambiar la orientación, se introduce la propiedad del vector `up` en la clase `Plane`. El siguiente fragmento de código muestra cómo cambiar la orientación del plano:

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
