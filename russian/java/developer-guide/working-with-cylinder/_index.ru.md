---
title: Работа с цилиндром
type: docs
weight: 100
url: /ru/java/working-with-cylinder/
description: Aspose.3D for Java позволяет настроить верх цилиндра со смещением. Для того, чтобы использовать эту функциональность, вы можете использовать метод setOffsetTop() класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for Java позволяет настроить верх цилиндра со смещением. Чтобы использовать эту функциональность, вы можете использовать метод `setOffsetTop()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



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

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

У левого есть OffsetTop (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
#  **Настроить ShearBottom**
Aspose.3D for Java позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `setShearBottom()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:



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

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет ShearBottom до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for Java позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете использовать свойство `setGenerateFanCylinder()` класса `Cylinder` до `true`. Следующий фрагмент кода показывает, как использовать эту функциональность:



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

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет GenerateFanCylinder = false, а правый-GenerateFanCylinder = true.
