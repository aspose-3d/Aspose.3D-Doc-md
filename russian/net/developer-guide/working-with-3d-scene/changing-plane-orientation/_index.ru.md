---
title: Изменение ориентации плоскости
type: docs
weight: 40
url: /ru/net/changing-plane-orientation/
description: Aspose.3D for .NET позволяет изменять ориентацию сцены. Для того чтобы изменить ориентацию, в классе плоскости вводится свойство вектора вверх.
---
##  **Изменение ориентации плоскости**
Aspose.3D for .NET позволяет изменять ориентацию сцены. Чтобы изменить ориентацию, в класс `Plane` вводится свойство `Up` vector. Следующий фрагмент кода показывает, как изменить ориентацию самолета:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
