---
title: 在 3D 文档中添加动画属性并设置目标相机
type: docs
weight: 10
url: /zh/python-net/add-animation-property-and-setup-target-camera-in-3d-document/
description: 在 Aspose.3D 中，对象动画实际上是对属性进行动画处理的关键帧动画。要对属性进行动画处理，您需要一个将属性的组件映射到不同曲线的CurveMapping实例，例如，Vector3属性可以有3个组件X/Y/Z，这将在CurveMapping中设置三个通道，每个通道都可以有一组曲线。
---
##  **在 3D 文档中添加动画属性**
Aspose.3D for Python via .NET 支持渲染动画场景。本文介绍移动对象的先决条件。
###  **移动立方体的位置**
{{% alert color="primary" %}}

代码中正在使用 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类对象。我们可以 [创建一个网格类对象，如在那里叙述](/3d/zh/net/create-and-read-an-existing-3d-scene/)，它必须动画节点的本地翻译属性: [将转换添加到节点](/3d/zh/net/adding-transformation-to-the-node/)。

{{% /alert %}}

在 Aspose.3D 中，对象动画实际上是对属性进行动画处理的关键帧动画。要对属性进行动画处理，您需要一个将属性的组件映射到不同曲线的 `CurveMapping` 实例，例如，一个 `Vector3` 属性可以有3个组件 `X`/`Y`/`Z`，这将在 `CurveMapping` 中设置三个通道，每个通道可以有一组 `Curve`。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-PropertyToDocument-AddAnimationPropertyToDocument.py" >}}
##  **在 3D 文件中设置目标相机**
Aspose.3D for Python via .NET 提供在 3D 文件中设置目标相机。在某些文件格式中，灯光/摄像机支持目标，这允许灯光/摄像机始终面向指定节点，这在动画中很有用。

{{% alert color="primary" %}}

代码中正在使用 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 、 [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera) 、 [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) 和 [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) 类。为了保存场景，使用 [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) 方法，它接受一个包含完整路径和 [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) 参数的文件名。

{{% /alert %}}

在下面的示例中，目标和相机在 3D 文件中设置:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-SetupTargetAndCamera-SetupTargetAndCamera.py" >}}
