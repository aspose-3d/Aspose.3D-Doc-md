---
title: 将网格转换为三角形网格，将原始形状转换为网格
type: docs
weight: 20
url: /zh/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose。3D for Java API 支持使用顶点的自定义内存布局将网格转换为三角形网格。顶点的自定义内存布局由代码示例中的VertexDeclaration类动态定义。
---
##  **使用顶点的自定义内存布局将网格转换为三角形网格**
Aspose。3D for Java API 支持使用顶点的自定义内存布局将网格转换为三角形网格。顶点的自定义内存布局由代码示例中的 `VertexDeclaration` 类动态定义。

{{% alert color="primary" %}}

此帮助主题从框和球体创建网格，以保持代码的全面和简短。开发人员可以按照以下帮助主题中的说明手动构建网格: [创建 3D 立方体网格](/3d/zh/java/create-3d-mesh-and-scene/)。

{{% /alert %}}

开发人员可能会将网格转换为三角形网格，因为任何复杂 (表面) 结构都可以表示为一堆三角形。三角形是最原子的几何形状。因此，它几乎被用作任何东西的基础。此代码示例使用自定义内存布局将框转换为三角形网格。



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
##  **将原始形状转换为网格**
Aspose.3D for Java API 支持将任何基本形状转换为网格。原始形状包括最基本的和使用过的对象，如长方体、球体、平面、圆柱体和圆环。

{{% alert color="primary" %}}

在导出为任何 3D 文件格式时，任何实现接口IMeshConvertible的类都可以转换为mesh。

{{% /alert %}}
###  **将球体原语转换为网格**
球体是三维空间中完美的圆形几何物体，从运动球到太空中的行星无处不在。让我们使用球体原语来创建网格。
下面的代码示例将球体转换为网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
###  **将框转换为网格**
盒子描述了各种容器和容器，这些容器和容器永久用作存储或临时使用，通常用于运输内容物。让我们使用框原语来创建网格。下面的代码示例将框转换为网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
###  **将平面转换为网格**
平面无限延伸而没有厚度。一个平面的例子是坐标平面。让我们使用平面原语创建网格。下面的代码示例将平面转换为网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
###  **将圆柱体转换为网格**
圆柱体是最基本的曲线几何形状之一，由与给定直线 (圆柱体的轴) 相距固定距离的点形成的表面。它可以在许多地方使用，例如作为房屋前面的支柱或汽车驱动轴。让我们使用圆柱原语创建网格。下面的代码示例将圆柱体转换为网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
###  **将圆环转换为网格**
圆环是通过在三维空间中绕与圆共面的轴旋转圆而产生的旋转表面。如果旋转轴不接触圆，则表面呈环形，称为圆环。让我们使用圆环原语来创建网格。下面的代码示例将圆环转换为网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
