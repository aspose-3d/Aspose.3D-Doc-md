---
title: 在立方体上设置法线或紫外线，并将材料添加到3D实体
type: docs
weight: 60
url: /zh/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java提供管理几何形状上的法线和UV。网格存储每个顶点，空间位置及其法线的关键属性，称为垂直于原始表面的向量。法线主要是阴影计数，应该是单位向量。大多数网格格式还支持某种形式的UV坐标，该坐标是 “展开” 网格的单独2D表示，以显示要应用于网格的不同多边形的二维纹理贴图的哪个部分。
---
{{% alert color="primary" %}}

Aspose.3D for Java提供管理几何形状上的法线和UV。网格存储每个顶点，空间位置及其法线的关键属性，称为垂直于原始表面的向量。法线主要是阴影计数，应该是单位向量。大多数网格格式还支持某种形式的UV坐标，该坐标是 “展开” 网格的单独2D表示，以显示要应用于网格的不同多边形的二维纹理贴图的哪个部分。

{{% /alert %}} {{% alert color="primary" %}}

代码中使用了`Mesh`类对象。我们可以[创建一个网格类对象，此处叙述](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)然后通过创建3D场景将节点指向网格几何。

{{% /alert %}}
## **创建正常向量**
为了在照明上具有良好的视觉效果，我们需要为每个顶点指定法线信息。为了拥有更好的细节，我们还可以使用法线和漫射贴图 (使用阴影/镜面贴图) 来执行每像素的法线/颜色。VertexElement可以实现每个顶点的信息，例如法线或顶点颜色。在Aspose.3D中，我们可以将额外的信息映射到控制点/多边形顶点/多边形/边，一个示例来定义顶点的法线:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


8个法线向量直接映射到8个控制点，在接下来的例子中，我们将演示一个更复杂的场景。
## **创建UV坐标**
在这里，我们只定义了4个UV坐标，但是通过使用索引将它们应用于24个多边形顶点 (每个多边形6面 * 4个顶点)。
该Aspose.3D提供了5种映射模式:

- **控制点**-每个数据都映射到几何图形的控制点。
- **多边形顶点**-数据映射到多边形的顶点。
- **多边形**-数据映射到多边形。
- **边缘**-数据被映射到边缘。
- **全部相同**-映射到整个几何图形的一个数据。



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **将材质添加到3D对象**
Aspose.3D for Java允许开发人员使用着色算法进行精确的着色和高光。Phong具有多个map输入，我们可以使用它们来屏蔽对节点的影响。基于物理的渲染 (PBR) 考虑了对象的某些物理属性，这种方法提供了现实世界中材料的外观。
### **立方体纹理Phong材料**
当UV坐标准备使用时，我们可以通过使用材料在网格表面上施加纹理。只有顶点颜色不能描述表面的细节，这就是材料的用途。以下是将Phong材质附加到多维数据集节点的示例:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


我们指定了漫射纹理映射和带有光泽参数的镜面颜色。
### **将基于物理的渲染 (PBR) 材料应用于盒子**
PBR在游戏引擎视觉效果中起着关键作用，它通过亮度的衰减和反射光的散射来高效逼真地渲染光和表面之间的相互作用。开发人员可以使用Aspose.3D API将PBR材质应用于场景中的3D对象。这个代码示例演示了如何创建一个Box对象，然后应用PBR材质。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
