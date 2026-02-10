---
title: Cylinder ile king orking
type: docs
weight: 100
url: /tr/java/working-with-cylinder/
description: Aspose.3D for Java bir silindirin ofset üstünü özelleştirmeye izin verir. Bu işlevselliği kullanmak için, silindir sınıfının setoffsettop () yöntemini kullanabilirsiniz.
---
#  **Oustomize ffffset Top**
Aspose.3D for Java allows customizing Offset Top of a cylinder. In order to use this functionality, you can use `setOffsetTop()` method of `Cylinder` class. The following code snippet shows how to customize Offset Top:



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

! [Todo: image_alt_text](working-with-cylinder_1.png)

To sol bir Offsetop op set (5, 3, 0), üst kapak taşındı ve tüm gövde de etkilenir görmek kolaydır.
#  **Customize hearhearhearottom**
Aspose.3D for Java allows customizing shear bottom of a cylinder. In order to use this functionality, you can use `setShearBottom()` property of `Cylinder` class. The following code snippet shows how to customize Shear Bottom:



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

! [Todo: image_alt_text](working-with-cylinder_2.png)

To sol silindir sağ bir sıra silindir iken Shearhearottom (0, 0.83) vardır.
#  **Create Fan-Cylinder**
Aspose.3D for Java allows creating a fan cylinder. In order to use this functionality, you can `setGenerateFanCylinder()` property of `Cylinder` class to `true`. The following code snippet shows how to use this functionality:



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

! [Todo: image_alt_text](working-with-cylinder_3.png)

To sol silindir GenerateFanCylinder = yanlış ve doğru olanı enerenerateeneran. ylinder = doğrudur.
