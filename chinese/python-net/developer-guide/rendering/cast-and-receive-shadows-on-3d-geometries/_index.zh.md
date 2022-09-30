---
title: 在3D几何图形上投射和接收阴影
type: docs
weight: 10
url: /zh/python-net/cast-and-receive-shadows-on-3d-geometries/
description: 通常，一些3D文件格式可以像FBX一样将阴影相关设置存储在几何体中。使用Aspose.3D进行Python via .NET，开发者可以通过从光源的视点映射阴影来渲染图像。图像质量取决于光源，仰角和相机与几何物体之间的距离。
---
{{% alert color="primary" %}}

通常，一些3D文件格式可以像FBX一样将阴影相关设置存储在几何体中。使用[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/),开发人员可以通过从光源的角度映射阴影来渲染图像。图像质量取决于光源，仰角和相机与几何物体之间的距离。

{{% /alert %}}
## **投射并接收阴影**
默认情况下，场景中的所有对象都会从光源投射阴影。开发人员还可以在对象表面中的每个对象的基础上接收阴影。此代码示例揭示了如何设置光和相机对象的位置。它还创建了一个平面，并放置了具有不同颜色和阴影设置的三个对象。

所有几何形状都有`cast_shadows = True`和`receive_shadows = True`，红色框和圆环的阴影投射到飞机上，红色框不会接收阴影，蓝色框不会投射阴影。
### **编程示例**
此代码示例对3D几何图形进行投射和接收阴影。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**渲染结果**

![todo: 图像_alt_文本](cast-and-receive-shadows-on-3d-geometries_1.png)
