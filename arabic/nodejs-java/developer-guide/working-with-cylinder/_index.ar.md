---
title: Working مع Cيندر
type: docs
weight: 100
url: /ar/nodejs-java/working-with-cylinder/
description: يسمح Aspose.3D for Node.js via Java بتخصيص أعلى إزاحة للأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام طريقة setOffsetTop() لفئة الأسطوانة.
---
#  **Customize ffffset op op**
يسمح Aspose.3D for Node.js via Java بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام طريقة `setOffsetTop()` لفئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder1 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Set OffsetTop
cylinder1.setOffsetTop(new aspose.threed.Vector3(5, 3, 0));

// Create ChildNode
var node1=scene.getRootNode().createChildNode(cylinder1);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Initialize second cylinder without customized OffsetTop
var cylinder2 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
scene.getRootNode().createChildNode(cylinder2);

// Save
scene.save("CustomizedOffsetTopCylinder.obj");

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_1.png)

Tترك واحد لديه ffffsetTop مجموعة إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله أيضا يتأثر.
#  **Customize hearالموقد العثماني**
يسمح Aspose.3D for Node.js via Java بتخصيص أسفل قص الأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية `setShearBottom()` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:

{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Create cylinder 1
var cylinder1 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Customized shear bottom for cylinder 1
cylinder1.setShearBottom(new aspose.threed.Vector2(0, 0.83));

// Add cylinder 1 to the scene
var node1=scene.getRootNode().createChildNode(cylinder1);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Create cylinder 2
var cylinder2 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Add cylinder to without a ShearBottom to the scene
scene.getRootNode().createChildNode(cylinder2);

// Save scene
scene.save("CustomizedShearBottomCylinder.obj");

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_2.png)

Tترك اسطوانة لديه hearhearBأوتوم إلى (0 ، 0.83) في حين أن الحق هو اسطوانة عادية.
#  **Create an an-Cylinder**
Aspose.3D for Node.js via Java يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك `setGenerateFanCylinder()` ملكية من فئة `Cylinder` إلى `true`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:

{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Create a cylinder
var fan  =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Set GenerateGanCylinder to true
fan.setGenerateFanCylinder(true);

// Set ThetaLength
fan.setThetaLength(aspose.threed.MathUtils.toRadian(270.0));

// Create ChildNode
var node1=scene.getRootNode().createChildNode(fan);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Create a cylinder without a fan
var nonfan  =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
scene.getRootNode().createChildNode(nonfan);

// Save scene
scene.save("CreateFanCylinder.obj");

{{< /highlight >}}

! [Todo: image_ altttext](working-with-cylinder_3.png)

Tانه ترك اسطوانة لديها enerenerateFanCylinder = كاذبة واليمين واحد لديه enerenerateFanCylinder = صحيح.
