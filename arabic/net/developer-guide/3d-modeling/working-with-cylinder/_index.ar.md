---
title: Working مع Cيندر
type: docs
weight: 130
url: /ar/net/working-with-cylinder/
description: Aspose.3D for .NET يسمح بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية الإزاحة لفئة الأسطوانة.
---
#  **Customize ffffset op op**
Aspose.3D for .NET يسمح بتخصيص أعلى إزاحة للأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام خاصية `Offset` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Initialize cylinder
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Set OffsetTop
cylinder1.OffsetTop = new Vector3(5, 3, 0);
// Create ChildNode
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Intialze second cylinder without customized OffsetTop
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.RootNode.CreateChildNode(cylinder2);
// Save
scene.Save("CustomizedOffsetTopCylinder.obj");

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_1.png)

Tترك واحد لديه ffffsetTop مجموعة إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله أيضا يتأثر.
#  **Customize hearالموقد العثماني**
Aspose.3D for .NET يسمح بتخصيص قاع قص الأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام خاصية `ShearBottom` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Create cylinder 2
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.RootNode.CreateChildNode(cylinder2);
// Save scene
scene.Save("CustomizedShearBottomCylinder.obj");


{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_2.png)

The left cylinder has `ShearBottom` to (0, 0.83) while the right one is an ordinal cylinder.
#  **Create an an-Cylinder**
Aspose.3D for .NET يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك تعيين خاصية `GenerateFanCylinder` لفئة `Cylinder` على `true`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Create cylinder 2
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.RootNode.CreateChildNode(cylinder2);
// Save scene
scene.Save("CustomizedShearBottomCylinder.obj");


{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_3.png)

تحتوي الأسطوانة اليسرى على `GenerateFanCylinder = false` ولدى الأسطوانة اليمنى `GenerateFanCylinder = true`.
