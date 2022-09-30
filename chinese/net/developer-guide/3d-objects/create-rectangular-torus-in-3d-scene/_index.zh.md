---
title: 在3D场景中创建矩形圆环
type: docs
weight: 50
url: /zh/net/create-rectangular-torus-in-3d-scene/
description: 使用Aspose.3D for .NET API，开发人员可以创建3D对象，然后以任何支持的3D格式保存3D场景。
---
{{% alert color="primary" %}} 

使用[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API，开发人员可以创建3D对象，然后以任何支持的3D格式保存3D场景。

{{% /alert %}} 
## **矩形圆环**
我们添加了`RectangularTorus`类，它允许开发人员将参数化的矩形圆环放入场景中，这可以在将场景保存为不同支持的文件格式期间转换为序数网格/三角形网格。

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

生成的矩形圆环如下所示:

![todo: 图像_alt_文本](create-rectangular-torus-in-3d-scene_1.png)
