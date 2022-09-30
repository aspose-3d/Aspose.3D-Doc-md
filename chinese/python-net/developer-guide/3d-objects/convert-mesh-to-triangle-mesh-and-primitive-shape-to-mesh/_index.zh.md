---
title: 将网格转换为三角形网格，将原始形状转换为网格
type: docs
weight: 30
url: /zh/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D Python via .NET API允许开发人员使用顶点的自定义内存布局将任何网格对象转换为三角形网格。Vertex的自定义内存布局是使用Struct或在代码示例中由VertexDeclaration类动态定义的。
---
## **使用顶点的自定义内存布局将网格转换为三角形网格**
[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/)API允许开发人员使用顶点的自定义内存布局将任何网格对象转换为三角形网格。Vertex的自定义内存布局是使用结构或代码示例中的[`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration)类动态定义的。

{{% alert color="primary" %}}

此帮助主题从框和球体创建网格，以保持代码的全面和简短。开发人员可以按照本帮助主题中的叙述手动构造网格:[创建3D立方体网格](/3d/zh/python-net/create-3d-mesh-and-scene/)。

{{% /alert %}}

这些示例显示了如何:

- [使用顶点的自定义内存布局 (在结构中定义) 将球体转换为三角形网格](/3d/zh/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/)。
- [使用顶点的自定义内存布局将框转换为三角形网格 (由VertexDeclaration类定义)](/3d/zh/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/)。
### **转换网格**
开发人员可能会将网格转换为三角形网格，因为任何复杂 (表面) 结构都可以表示为一堆三角形。三角形是最原子的几何形状。因此，它几乎被用作任何东西的基础。
### **访问三角形网格的顶点**
开发人员可以访问索引，实际顶点，合并前的顶点以及内存中顶点的总字节。

下面的示例使用自定义内存布局将球体转换为三角形网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




下面的示例使用自定义内存布局将框转换为三角形网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
## **将 “原始” 转换为 “网格”**
使用Aspose.3D进行Python via .NET，开发人员可以将任何原始对象转换为网格。原语包括许多最基本和最常用的对象，例如盒子，球体，平面，圆柱体和圆环。

{{% alert color="primary" %}}

实现接口IMeshConvertible的任何类都可以在导出为任何3D文件格式时转换为网格。

{{% /alert %}}
### **将 “sphere” 转换为“ 网格”**
球体是三维空间中完美的圆形几何物体，从运动球到太空中的行星无处不在。让我们使用球体原语来创建网格。
下面的代码示例将球体转换为网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.py" >}}
### **将 “框” 转换为 “网格”**
盒子描述了各种容器和容器，这些容器和容器永久用作存储或临时使用，通常用于运输内容物。让我们使用框原语来创建网格。下面的代码示例将框转换为网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.py" >}}
### **将 “飞机” 转换为 “网格”**
平面无限延伸而没有厚度。一个平面的例子是坐标平面。让我们使用平面原语创建网格。下面的代码示例将平面转换为网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.py" >}}
### **将 “圆柱体” 转换为 “网格”**
圆柱体是最基本的曲线几何形状之一，由与给定直线 (圆柱体的轴) 相距固定距离的点形成的表面。它可以在许多地方使用，例如作为房屋前面的支柱或汽车驱动轴。让我们使用圆柱原语创建网格。下面的代码示例将圆柱体转换为网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.py" >}}
### **将 “圆环” 转换为 “网格”**
圆环是通过在三维空间中绕与圆共面的轴旋转圆而产生的旋转表面。如果旋转轴不接触圆，则表面呈环形，称为圆环。让我们使用圆环原语来创建网格。下面的代码示例将圆环转换为网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.py" >}}
