---
title: Работа с цилиндром
type: docs
weight: 100
url: /ru/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java позволяет настроить Offset Top цилиндра. Для того, чтобы использовать эту функциональность, вы можете использовать метод setOffsetTop() класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for Node.js via Java позволяет настроить Offset Top цилиндра. Чтобы использовать эту функциональность, вы можете использовать метод `setOffsetTop()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



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

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

У левого есть OffsetTop (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
#  **Настроить ShearBottom**
Aspose.3D for Node.js via Java позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `setShearBottom()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:

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

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет ShearBottom до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for Node.js via Java позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете использовать свойство `setGenerateFanCylinder()` класса `Cylinder` до `true`. Следующий фрагмент кода показывает, как использовать эту функциональность:

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

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет GenerateFanCylinder = false, а правый-GenerateFanCylinder = true.
