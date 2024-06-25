---
title: Cylinder ile king orking
type: docs
weight: 100
url: /tr/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java, bir silindirin ofset üstünü özelleştirmeye izin verir. Bu işlevselliği kullanmak için, silindir sınıfının setoffsettop () yöntemini kullanabilirsiniz.
---
#  **Oustomize ffffset Top**
Aspose.3D for Node.js via Java allows customizing Offset Top of a cylinder. In order to use this functionality, you can use `setOffsetTop()` method of `Cylinder` class. The following code snippet shows how to customize Offset Top:



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

! [Todo: image_alt_text](working-with-cylinder_1.png)

To sol bir Offsetop op set (5, 3, 0), üst kapak taşındı ve tüm gövde de etkilenir görmek kolaydır.
#  **Customize hearhearhearottom**
Aspose.3D for Node.js via Java allows customizing shear bottom of a cylinder. In order to use this functionality, you can use `setShearBottom()` property of `Cylinder` class. The following code snippet shows how to customize Shear Bottom:

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

! [Todo: image_alt_text](working-with-cylinder_2.png)

To sol silindir sağ bir sıra silindir iken Shearhearottom (0, 0.83) vardır.
#  **Create Fan-Cylinder**
Aspose.3D for Node.js via Java allows creating a fan cylinder. In order to use this functionality, you can `setGenerateFanCylinder()` property of `Cylinder` class to `true`. The following code snippet shows how to use this functionality:

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

! [Todo: image_alt_text](working-with-cylinder_3.png)

To sol silindir GenerateFanCylinder = yanlış ve doğru olanı enerenerateeneran. ylinder = doğrudur.
