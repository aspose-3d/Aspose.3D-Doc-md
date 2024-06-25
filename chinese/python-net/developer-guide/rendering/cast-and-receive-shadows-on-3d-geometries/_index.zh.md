---
title: 在 3D 个几何体上投射和接收阴影
type: docs
weight: 10
url: /zh/python-net/cast-and-receive-shadows-on-3d-geometries/
description: 通常，某些 3D 文件格式可以在几何图形 (如 FBX) 中存储与阴影相关的设置。使用 Aspose.3D for Python via .NET，开发人员可以通过从光源的视点映射阴影来渲染图像。图像质量取决于光源、仰角和相机与几何对象之间的距离。
---
{{% alert color="primary" %}}

通常，某些 3D 文件格式可以在几何图形 (如 FBX) 中存储与阴影相关的设置。使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/)，开发人员可以通过从光源的视点映射阴影来渲染图像。图像质量取决于光源、仰角和相机与几何对象之间的距离。

{{% /alert %}}
##  **投射并接收阴影**
默认情况下，场景中的所有对象都会从光源投射阴影。开发人员还可以在对象表面中的每个对象的基础上接收阴影。此代码示例揭示了如何设置光和相机对象的位置。它还创建了一个平面，并放置了具有不同颜色和阴影设置的三个对象。

所有几何都有 `cast_shadows = True` 和 `receive_shadows = True`，红色框和圆环的阴影投射到平面上，红色框不会接收阴影，蓝色框不会投射阴影。
###  **编程示例**
此代码示例在 3D 个几何图形上投射和接收阴影。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**渲染结果**

![todo: 图像 _ alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
