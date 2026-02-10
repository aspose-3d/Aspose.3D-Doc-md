---
title: Cمعلقة lane لين O
type: docs
weight: 40
url: /ar/python-net/changing-plane-orientation/
description: يسمح Aspose.3D for Python via .NET بتغيير اتجاه المشهد. من أجل تغيير الاتجاه ، يتم إدخال خاصية المتجه لأعلى في فئة الطائرة.
---
#  **Cمعلقة lane لين O**
يسمح Aspose.3D for Python via .NET بتغيير اتجاه المشهد. لتغيير الاتجاه ، تم إدخال خاصية المتجه `up` في فئة `Plane`. يظهر مقتطف الكود التالي كيفية تغيير اتجاه الطائرة:

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
