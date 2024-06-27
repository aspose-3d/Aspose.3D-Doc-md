---
title: 与气缸一起工作
type: docs
weight: 100
url: /zh/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用Cylinder类的setOffsetTop() 方法。
---
#  **自定义偏移顶部**
Aspose.3D for Node.js via Java 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用 `Cylinder` 类的 `setOffsetTop()` 方法。以下代码段显示了如何自定义偏移顶部:



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

![todo: 图像 _ alt_text](working-with-cylinder_1.png)

左边的OffsetTop设置为 (5,3，0)，很容易看到顶盖移动了，整个躯干也受到了影响。
#  **自定义剪切底部**
Aspose.3D for Node.js via Java 允许自定义圆柱体的剪切底部。为了使用此功能，您可以使用 `Cylinder` 类的 `setShearBottom()` 属性。以下代码段显示了如何自定义剪切底部:

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

![todo: 图像 _ alt_text](working-with-cylinder_2.png)

左圆柱体具有剪切底部到 (0，0.83)，而右圆柱体是序数圆柱体。
#  **创建风扇气缸**
Aspose.3D for Node.js via Java 允许创建一个风扇圆柱体。为了使用此功能，您可以将 `Cylinder` 类的 `setGenerateFanCylinder()` 属性设置为 `true`。以下代码段显示了如何使用此功能:

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

![todo: 图像 _ alt_text](working-with-cylinder_3.png)

左圆柱体具有GenerateFanCylinder = false，右圆柱体具有GenerateFanCylinder = true。
