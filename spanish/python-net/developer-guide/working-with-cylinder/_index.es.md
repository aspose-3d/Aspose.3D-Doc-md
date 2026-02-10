---
title: Trabajando con cilindro
type: docs
weight: 130
url: /es/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar la propiedad Offset de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for Python via .NET permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar la propiedad `offset` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



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

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene `offset_top` establecido en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for Python via .NET permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `shear_bottom` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



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

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene `shear_bottom` a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for Python via .NET permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede establecer la propiedad `generate_fan_cylinder` de la clase `Cylinder` en `True`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



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

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene `generate_fan_cylinder = False` y el derecho tiene `generate_fan_cylinder = True`.
