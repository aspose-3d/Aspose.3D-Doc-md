---
title: 在 3D 文档中添加动画属性并设置目标相机
type: docs
weight: 10
url: /zh/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: 在 Aspose.3D 中，对象动画实际上是对属性进行动画处理的关键帧动画。要对属性进行动画处理，您需要一个将属性的组件映射到不同曲线的CurveMapping实例，例如，Vector3属性可以有3个组件X/Y/Z，这将在CurveMapping中设置三个通道，每个通道都可以有一组曲线。
---
##  **在 3D 文档中添加动画属性**
Aspose.3D for .NET 支持渲染动画场景。本文介绍移动对象的先决条件。
###  **移动立方体的位置**
{{% alert color="primary" %}}

代码中正在使用 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类对象。我们可以 [创建一个网格类对象，如在那里叙述](/3d/zh/net/create-and-read-an-existing-3d-scene/)，它必须动画节点的本地翻译属性: [将转换添加到节点](/3d/zh/net/adding-transformation-to-the-node/)。

{{% /alert %}}

在 Aspose.3D 中，对象动画实际上是对属性进行动画处理的关键帧动画。要对属性进行动画处理，您需要一个将属性的组件映射到不同曲线的 `CurveMapping` 实例，例如，一个 `Vector3` 属性可以有3个组件 `X`/`Y`/`Z`，这将在 `CurveMapping` 中设置三个通道，每个通道可以有一组 `Curve`。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();             

// Each cube node has their own translation
Node cube1 = scene.RootNode.CreateChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.Transform.FindProperty("Translation");
            
// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale 
bindPoint.BindKeyframeSequence("X", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, 20.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 30.0f, Interpolation.Linear},
});

// Create the animation curve on Z component of the scale 
bindPoint.BindKeyframeSequence("Z", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, -10.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 0.0f, Interpolation.Linear},
});

// Save 3D scene in the supported file formats
scene.Save("PropertyToDocument.fbx");

{{< /highlight >}}
##  **在 3D 文件中设置目标相机**
Aspose.3D for .NET 提供在 3D 文件中设置目标相机。在某些文件格式中，灯光/摄像机支持目标，这允许灯光/摄像机始终面向指定节点，这在动画中很有用。

{{% alert color="primary" %}}

代码中正在使用 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 、 [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera) 、 [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) 和 [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) 类。要保存正在使用的 `Scene`，[`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) 方法，它接受具有完整路径和 [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) 参数的文件名。

{{% /alert %}}

在下面的示例中，目标和相机在 3D 文件中设置:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
// Set camera node translation
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity<Camera>().Target = scene.RootNode.CreateChildNode("target");
scene.Save("camera-test.3ds");

{{< /highlight >}}
