---
title: 改变平面方向
type: docs
weight: 40
url: /zh/net/changing-plane-orientation/
description: Aspose.3D for .NET 允许更改场景的方向。为了改变方向，在Plane类中引入了向上向量属性。
---
##  **改变平面方向**
Aspose.3D for .NET 允许更改场景的方向。为了改变方向，在 `Plane` 类中引入了 `Up` 向量属性。以下代码片段显示了如何更改平面的方向:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
