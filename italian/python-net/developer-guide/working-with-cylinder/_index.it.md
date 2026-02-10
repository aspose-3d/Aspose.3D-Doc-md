---
title: Lavorare con il cilindro
type: docs
weight: 130
url: /it/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare la proprietà Offset della classe Cilindro.
---
#  **Personalizza la parte superiore offset**
Aspose.3D for Python via .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `offset` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare Offset Top:



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

! [Todo: image_alt_text](working-with-cylinder_1.png)

Quello sinistro ha `offset_top` impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#  **Personalizza ShearBottom**
Aspose.3D for Python via .NET consente di personalizzare il fondo di taglio di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `shear_bottom` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare il fondo di taglio:



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

! [Todo: image_alt_text](working-with-cylinder_2.png)

Il cilindro sinistro ha `shear_bottom` a (0, 0,83) mentre quello destro è un cilindro ordinale.
#  **Crea Ventilatore-Cilindro**
Aspose.3D for Python via .NET consente di creare un cilindro della ventola. Per poter utilizzare questa funzionalità, puoi impostare la proprietà `generate_fan_cylinder` della classe `Cylinder` su `True`. Il seguente frammento di codice mostra come utilizzare questa funzionalità:



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

! [Todo: image_alt_text](working-with-cylinder_3.png)

Il cilindro sinistro ha `generate_fan_cylinder = False` e quello destro ha `generate_fan_cylinder = True`.
