---
title: Arbeta med cylinder
type: docs
weight: 130
url: /sv/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET tillåter anpassning av offset toppen av en cylinder. För att använda denna funktionalitet kan du använda Offset egenskap av Cylinderklass.
---
#  **Anpassa offset övrev**
Aspose.3D for Python via .NET tillåter anpassning av offset toppen av en cylinder. För att kunna använda denna funktionalitet, kan du använda `offset` egenskapen i `Cylinder` klassen. Följande kod snutt visar hur man anpassar Offset Top:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Initialize cylinder
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Set OffsetTop
cylinder1.offset_top = Vector3(5, 3, 0)
#  Create ChildNode
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Intialze second cylinder without customized OffsetTop
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Create ChildNode
scene.root_node.create_child_node(cylinder2)
#  Save
scene.save("data-dir" + "CustomizedOffsetTopCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

![todo:image_alt_text](working-with-cylinder_1.png)

Den vänstra har `offset_top` satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
#  **Anpassa shearBottom**
Aspose.3D for Python via .NET tillåter anpassning av skjuv botten i en cylinder. För att kunna använda denna funktionalitet, kan du använda `shear_bottom` egenskapen i `Cylinder` klassen. Följande kodutdrag visar hur man anpassar skjuv nedre:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector2, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Create cylinder 1
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Customized shear bottom for cylinder 1
cylinder1.shear_bottom = Vector2(0, 0.83)
#  Add cylinder 1 to the scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

![todo:image_alt_text](working-with-cylinder_2.png)

Den vänstra cylindern har `shear_bottom` till (0, 0.83) medan den högra är en ordinarie cylinder.
#  **Skapa fläkt- cylinder**
Aspose.3D for Python via .NET tillåter att skapa en fläktcylinder. För att kunna använda denna funktionalitet kan du ställa in `generate_fan_cylinder` egenskap av `Cylinder` klass till `True`. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector2, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Create cylinder 1
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Customized shear bottom for cylinder 1
cylinder1.shear_bottom = Vector2(0, 0.83)
#  Add cylinder 1 to the scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

![todo:image_alt_text](working-with-cylinder_3.png)

Den vänstra cylindern har `generate_fan_cylinder = False` och den högra har `generate_fan_cylinder = True`.
