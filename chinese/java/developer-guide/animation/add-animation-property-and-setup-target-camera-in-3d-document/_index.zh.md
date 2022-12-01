---
title: 在3D文档中添加动画属性和设置目标摄像机
type: docs
weight: 10
url: /zh/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java支持渲染动画场景。本文介绍了移动对象的先决条件。
---
## **在3D文档中添加动画属性**
Aspose.3D for Java支持渲染动画场景。本文介绍了移动对象的先决条件。
### **移动立方体的位置**
{{% alert color="primary" %}}

代码中使用了`Mesh`类对象。我们可以[创建一个网格类对象，如在那里叙述](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)它也必须为节点的本地翻译属性设置动画:[将转换添加到节点](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/)。

{{% /alert %}}

在Aspose.3D for Java API中，动画实例实际上是对属性进行动画处理的关键帧动画。为了动画属性，您需要一个`CurveMapping`实例，该实例将属性的组件映射到不同的曲线，例如，`Vector3`属性可以具有3个组件`X`/`Y`/`Z`，这将在`CurveMapping`中设置三个通道，每个通道可以具有一组`Curve`。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **在3D文件中设置目标摄像机**
Aspose.3D for Java提供在3D文件中设置目标相机。在某些文件格式中，light/camera支持目标，这允许light/camera始终面对指定的节点，这在动画中很有用。

{{% alert color="primary" %}}

代码中使用了`Scene`、`Camera`、`Node`和`Transform`类。为了保存`Scene`，正在使用`Scene.save`方法，它接受带有完整路径和`FileFormat`参数的文件名。

{{% /alert %}}

在下面的示例中，目标和摄像机设置在3D文件中:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
