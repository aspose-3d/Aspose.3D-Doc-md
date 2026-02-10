---
title: Working مع Cيندر
type: docs
weight: 130
url: /ar/python-net/working-with-cylinder/
description: يسمح Aspose.3D for Python via .NET بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية الإزاحة لفئة الأسطوانة.
---
#  **Customize ffffset op op**
يسمح Aspose.3D for Python via .NET بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية `offset` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



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

! [Todo: image_ altttext](working-with-cylinder_1.png)

تم ضبط `offset_top` على اليسار (5 ، 3 ، 0) ، ومن السهل رؤية أن الغطاء العلوي قد تحرك وأن الجذع بأكمله قد تأثر أيضًا.
#  **Customize hearالموقد العثماني**
يسمح Aspose.3D for Python via .NET بتخصيص أسفل قص الأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية `shear_bottom` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:



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

! [Todo: image_ altttext](working-with-cylinder_2.png)

The left cylinder has `shear_bottom` to (0, 0.83) while the right one is an ordinal cylinder.
#  **Create an an-Cylinder**
Aspose.3D for Python via .NET يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك تعيين خاصية `generate_fan_cylinder` لفئة `Cylinder` إلى `True`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



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

! [Todo: image_ altttext](working-with-cylinder_3.png)

تحتوي الأسطوانة اليسرى على `generate_fan_cylinder = False` ولدى الأسطوانة اليمنى `generate_fan_cylinder = True`.
