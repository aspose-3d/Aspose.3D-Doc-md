---
title: 创建3D网格和场景
type: docs
weight: 40
url: /zh/java/create-3d-mesh-and-scene/
description: 网格由一组控制点和根据需要的许多n边多边形定义。本文介绍了如何定义网格。
---
## **创建3D立方体网格**
根据需要，`Mesh`由一组控制点和许多n边多边形定义。本文介绍了如何定义`Mesh`。

为了创建`Mesh`曲面，我们需要定义控制点和多边形，如下所示:

- [定义控制点](/3d/zh/java/create-3d-mesh-and-scene-html/)
- [使用PolygonBuilder类创建多边形](/3d/zh/java/create-3d-mesh-and-scene-html/)
- [创建多边形](/3d/zh/java/create-3d-mesh-and-scene-html/)

以下是将Phong材质附加到多维数据集节点的示例:
### **定义控制点**
网格由一组空间中的控制点组成，多边形用于描述网格表面，要创建网格，我们需要定义控制点:

{{% alert color="primary" %}} 

Aspose.3D中所有几何图形的控制点都使用齐次坐标，因此在示例代码中`Vector4`而不是`Vector3`。

{{% /alert %}} 

**示例:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



### **创建多边形**
控制点不可渲染，为了使立方体可见，我们需要在每一侧定义多边形:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



### **使用PolygonBuilder类创建多边形**
我们也可以用PolygonBuilder类的顶点定义多边形:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

现在完成了，为了使网格可见，我们需要为它准备一个节点。
## **如何三角剖分网格**
三角网格对于游戏行业很有用，因为三角形是GPU硬件支持的唯一受支持的基元 (非三角数据在驱动程序级别进行三角划分，在实时渲染中效率低下)

{{% alert color="primary" %}} 

在此版本中，我们仅对多边形进行了三角化，因为3ds文件导出需要它，在此过程中会丢失法线/uv和其他顶点元素，因此将来可以实现。

{{% /alert %}} 

在此示例中，我们通过导入FBX文件来三角化网格，并将其保存为FBX格式。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
## **创建3D多维数据集场景**
本主题演示如何将网格几何添加到3D场景。示例代码以支持的文件格式放置多维数据集并保存3D场景。
### **创建多维数据集节点**
节点是不可见的，但是可以渲染附加到该节点的几何图形。

{{% alert color="primary" %}} 

在代码中正在使用Mesh类对象。我们可以[创建一个网格类对象，如在那里叙述](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh)。

{{% /alert %}} 

**示例:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

注意: CAD/CAM软件中通常会忽略根节点上的实体，因此我们需要创建一个新节点来渲染几何图形。

{{% /alert %}}
