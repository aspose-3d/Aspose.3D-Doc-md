---
title: Работа с цилиндром
type: docs
weight: 130
url: /ru/net/working-with-cylinder/
description: Aspose.3D for .NET позволяет настроить верх цилиндра со смещением. Для того, чтобы использовать эту функциональность, вы можете использовать свойство Offset класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for .NET позволяет настроить верх цилиндра со смещением. Чтобы использовать эту функциональность, вы можете использовать свойство `Offset` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



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

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

У левого есть OffsetTop (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
#  **Настроить ShearBottom**
Aspose.3D for .NET позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `ShearBottom` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:



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

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет от `ShearBottom` до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for .NET позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете установить свойство `GenerateFanCylinder` класса `Cylinder` на `true`. Следующий фрагмент кода показывает, как использовать эту функциональность:



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

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет `GenerateFanCylinder = false`, а правый-`GenerateFanCylinder = true`.
