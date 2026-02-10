---
title: Working مع Cيندر
type: docs
weight: 100
url: /ar/java/working-with-cylinder/
description: Aspose.3D for Java يسمح بتخصيص أعلى إزاحة للأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام طريقة setOffsetTop() لفئة الأسطوانة.
---
#  **Customize ffffset op op**
Aspose.3D for Java يسمح بتخصيص أعلى إزاحة للأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام طريقة `setOffsetTop()` لفئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Create a scene
Scene scene = new Scene();
// Initialize cylinder
Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Set OffsetTop
cylinder1.setOffsetTop(new Vector3(5, 3, 0));
// Create ChildNode
scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);
// Initialize second cylinder without customized OffsetTop
Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.getRootNode().createChildNode(cylinder2);
// Save
scene.save(RunExamples.getDataDir()+ "CustomizedOffsetTopCylinder.obj", FileFormat.WAVEFRONTOBJ);
{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_1.png)

Tترك واحد لديه ffffsetTop مجموعة إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله أيضا يتأثر.
#  **Customize hearالموقد العثماني**
Aspose.3D for Java يسمح بتخصيص قاع قص الأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام خاصية `setShearBottom()` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.setShearBottom(new Vector2(0, 0.83));// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);
// Create cylinder 2
Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.getRootNode().createChildNode(cylinder2);
// Save scene
scene.save(RunExamples.getDataDir()+ "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_2.png)

Tترك اسطوانة لديه hearhearBأوتوم إلى (0 ، 0.83) في حين أن الحق هو اسطوانة عادية.
#  **Create an an-Cylinder**
Aspose.3D for Java يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك `setGenerateFanCylinder()` ملكية من فئة `Cylinder` إلى `true`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Jav
// Create a Scene
Scene scene = new Scene();
// Create a cylinder
Cylinder fan = new Cylinder(2, 2, 10, 20, 1, false);
// Set GenerateGanCylinder to true
fan.setGenerateFanCylinder(true);
// Set ThetaLength
fan.setThetaLength(MathUtils.toRadian(270.0));
// Create ChildNode
scene.getRootNode().createChildNode(fan).getTransform().setTranslation(10, 0, 0);
// Create a cylinder without a fan
Cylinder nonfan = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.getRootNode().createChildNode(nonfan);
// Save scene
scene.save(RunExamples.getDataDir()+ "CreateFanCylinder.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_3.png)

Tانه ترك اسطوانة لديها enerenerateFanCylinder = كاذبة واليمين واحد لديه enerenerateFanCylinder = صحيح.
