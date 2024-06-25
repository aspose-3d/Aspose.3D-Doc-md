---
title: 在 3D 文档中添加动画属性并设置目标相机
type: docs
weight: 10
url: /zh/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java 支持渲染动画场景。本文介绍移动对象的先决条件。
---
##  **在 3D 文档中添加动画属性**
Aspose.3D for Java 支持渲染动画场景。本文介绍移动对象的先决条件。
###  **移动立方体的位置**
{{% alert color="primary" %}}

代码中正在使用 `Mesh` 类对象。我们可以 [创建一个网格类对象，如在那里叙述](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)，它必须动画节点的本地翻译属性: [将转换添加到节点](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/)。

{{% /alert %}}

在 Aspose.3D for Java API 中，animation实例实际上是对属性进行动画处理的关键帧动画。为了动画属性，您需要一个 `CurveMapping` 实例，它将属性的组件映射到不同的曲线，例如，一个 `Vector3` 属性可以有3个组件 `X`/`Y`/`Z`，这将在 `CurveMapping` 中设置三个频道，每个频道可以有一组 `Curve`。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **在 3D 文件中设置目标相机**
Aspose.3D for Java 提供在 3D 文件中设置目标相机。在某些文件格式中，灯光/摄像机支持目标，这允许灯光/摄像机始终面向指定节点，这在动画中很有用。

{{% alert color="primary" %}}

代码中正在使用 `Scene` 、 `Camera` 、 `Node` 和 `Transform` 类。为了保存正在使用的 `Scene`，`Scene.save` 方法，它接受具有完整路径和 `FileFormat` 参数的文件名。

{{% /alert %}}

在下面的示例中，目标和相机在 3D 文件中设置:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
