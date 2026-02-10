---
title: 以球体半径工作
type: docs
weight: 110
url: /zh/net/working-with-radius-of-sphere/
description: 使用 Aspose.3D for .NET，您可以设置球体的获取半径。为了获取或设置半径，您可以使用Sphere类的半径属性。以下是设置球体半径的代码示例。
---
{{% alert color="primary" %}} 

19.4或更高版本支持此功能。

{{% /alert %}} 
##  **以球体半径工作**
使用 Aspose.3D for .NET，您可以设置球体的获取半径。为了获取或设置半径，您可以使用 `Sphere` 类的 `Radius` 属性。以下是设置球体半径的代码示例。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
