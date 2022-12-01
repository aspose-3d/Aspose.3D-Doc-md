---
title: 在立方体上设置法线或UV，并将材质添加到3D实体
type: docs
weight: 20
url: /zh/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: 如何在Aspose.3D中的网格上创建法线或uv数据。
---
{{% alert color="primary" %}}

Aspose.3D Python via .NET提供管理几何形状上的法线和UV。网格存储每个顶点的关键属性是其在空间中的位置及其法线 (垂直于原始表面的向量)。正常是主要的阴影计数。法线应该是单位向量。大多数网格格式还支持某种形式的UV坐标，该坐标是 “展开” 网格的单独2d表示，以显示要应用于网格的不同多边形的二维纹理贴图的哪个部分。

{{% /alert %}} {{% alert color="primary" %}}

代码中使用了`Mesh`类对象。我们可以[创建一个`Mesh`类对象，如在那里叙述](/3d/zh/python-net/create-3d-mesh-and-scene/)然后通过以下方式将节点指向网格几何[创建3D场景](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}
## **创建正常向量**
为了在照明上有良好的视觉效果，我们需要为每个顶点指定法线信息，为了有更好的细节，我们还可以使用法线和漫射贴图 (当然可以使用阴影/镜面贴图) 来执行每像素法线/颜色。通过`VertexElement`实现像法线或顶点颜色的每个顶点信息。在Aspose.3D中，我们可以将额外的信息映射到控制点/多边形顶点/多边形/边，一个示例来定义顶点的法线:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

8个法线向量直接映射到8个控制点，在接下来的例子中，我们将演示一个更复杂的场景。
## **创建UV坐标**
在这里，我们只定义了4个UV坐标，但是通过使用索引将它们应用于24个多边形顶点 (每个多边形6面 * 4个顶点)。
该Aspose.3D提供了5种映射模式:

- `CONTROL_POINT`-每个数据都映射到几何图形的控制点。
- `POLYGON_VERTEX`-数据被映射到多边形的顶点。
- `POLYGON`-数据被映射到多边形。
- `EDGE`-数据被映射到边缘。
- `ALL_SAME`-映射到整个几何图形的一个数据。



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
## **将材质添加到3D对象**
Aspose.3D Python via .NET允许开发人员使用着色算法进行精确的着色和高光。Phong具有多个map输入，我们可以使用它们来屏蔽对节点的影响。基于物理的渲染 (PBR) 考虑了对象的某些物理属性，这种方法提供了现实世界中材料的外观。
### **立方体纹理Phong材料**
当UV坐标准备使用时，我们可以通过使用材料在网格表面上施加纹理。只有顶点颜色不能描述表面的细节，这就是材料的用途。以下是将Phong材质附加到多维数据集节点的示例:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

我们指定了漫射纹理映射和带有光泽参数的镜面颜色。
### **将基于物理的渲染 (PBR) 材料应用于盒子**
PBR在游戏引擎视觉效果中起着关键作用，它通过亮度的衰减和反射光的散射来高效逼真地渲染光和表面之间的相互作用。开发人员可以使用Aspose.3D API将PBR材质应用于场景中的3D对象。这个代码示例演示了如何创建一个Box对象，然后应用PBR材质。

**.NET，C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
