---
title: 向节点添加转换
type: docs
weight: 10
url: /zh/java/adding-transformation-to-the-node/
description: Aspose。3D for Java API 支持在 3D 空间中旋转对象。有三种方法来定义对象在 3D 空间中的旋转，欧拉角，四元数和自定义矩阵，所有这些都由Transform类支持。
---
{{% alert color="primary" %}} 

Aspose。3D for Java API 支持在 3D 空间中旋转对象。有三种方法来定义对象在 3D 空间中的旋转，欧拉角，四元数和自定义矩阵，所有这些都由 `Transform` 类支持。

{{% /alert %}} 

TSR (平移/缩放/旋转) 在 3D 场景中最常用，我们提供了一个类 `Transform` 来访问 Aspose 中的这些。3D 仿射变换包括:

- 翻译
- 缩放
- 旋转
- 剪切映射
- 挤压映射

{{% alert color="primary" %}} 

代码中正在使用 `Mesh` 类对象。我们可以 [创建一个网格类对象，如在那里叙述](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene)。

{{% /alert %}} 
##  **按四元数旋转**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
##  **按欧拉角旋转**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
##  **自定义转换矩阵**
我们也可以直接使用矩阵:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
