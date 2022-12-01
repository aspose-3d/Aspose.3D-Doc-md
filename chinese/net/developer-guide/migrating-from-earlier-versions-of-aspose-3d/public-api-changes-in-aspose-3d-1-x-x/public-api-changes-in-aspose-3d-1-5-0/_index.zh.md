---
title: Aspose.3D中的公共API变化1.5.0
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-1-5-0/
---
**内容摘要**

- [将图元转换为网格并从图元3D模型创建场景](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [使用顶点的自定义内存布局将网格转换为三角形网格](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [分割网格](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [删除Distreet3DS格式。](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [添加Discreet3DS格式。](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [在类Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

本文档介绍了Aspose.3D API从1.4.0版到1.5.0版的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
### **将图元转换为网格并从图元3D模型创建场景**
**添加了各种类、方法和属性**

- **添加接口Aspose.ThreeD。实体。IMeshConvertible。** 
-实现此接口的任何类都可以在导出为任何3D文件格式时转换为网格。
- **添加类Aspose.ThreeD.Entities.Primitive。** 
-它是从实体类派生的，也是所有原始类的基类。
- **添加类Aspose.ThreeD.Entities.Box/Cylinder/Plane/Sphere/Torus.** 
-这些可以用来用简单原语定义场景。开发人员还可以将它们自动转换为网格。

原语包括许多最基本和最常用的对象，例如盒子，球体，平面，圆柱体和圆环。开发人员也可以将它们转换为网格以进行修改。这些帮助主题说明了如何做到这一点:[将图元转换为网格](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)和[将图元转换为网格](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **使用顶点的自定义内存布局将网格转换为三角形网格**
**添加了各种类、方法和属性**

- **添加类Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
-特里梅什/特里梅什<T>包含具有自定义内存布局的基于三角形的网格的定义，当开发人员要求将场景转换为自己的专有文件格式或渲染时，这很有用。
- **添加结构Aspose.ThreeD.实用程序.FVector2/FVector3/FVector4** 
-这些类在浮点数中呈现向量分量。只有少数现代GPU支持双精度矢量，单精度浮点类型在实时渲染世界中更受欢迎。这些替换将与原始Vector2/Vector3/Vector4共存，因为它们在Aspose.3D中扮演不同的角色。双精度主要用于存储模型的数据，因为它具有较小的累积误差。单精度主要用于渲染或用户自己的专有文件格式转换，因为它具有更好的接受度和性能。我们在Aspose.3D 1.5中引入了这组向量，因为我们添加了对自定义顶点布局的支持，其中将经常使用浮点向量。
- **添加属性类Aspose.ThreeD.实用程序.SemanticAttribute** 
-开发人员可以为vertex定义自定义结构，并使用此属性标记字段的语义。
- **添加类Aspose.ThreeD.实用程序.VertexDeclaration** 
-它描述了顶点的内存布局。
- **添加枚举Aspose.ThreeD。实用程序。VertexFieldDataType/VertexFieldSemantic** 
-这些枚举类型分别注释顶点字段的数据类型和语义。
- **添加类Aspose.ThreeD.实用程序.VertexField** 
-它描述了Vertex的自定义内存布局中的每个字段。
- **添加类Aspose.ThreeD.实用程序.Vertex** 
-可用于访问TriMesh/TriMesh中的原始顶点<T>

开发人员可以使用顶点的自定义内存布局将任何网格对象转换为三角形网格。图形软件包和硬件设备在三角形上的运行效率更高。此帮助主题说明了如何做到这一点:[使用顶点的自定义内存布局将网格转换为三角形网格](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **分割网格**
**添加了各种类、方法和属性**

- **添加枚举Aspose.ThreeD.实体.SplitMeshPolicy** 
-它指定了网格分割算法中使用的数据策略，我们支持两种策略，在子网格之间共享数据或每个子网格都有自己的数据 (仅使用的数据)。
- **将3个SplitMesh方法添加到Aspose.ThreeD.Entities.PolygonModifier类** 
1.通过材质定义将指定节点上的网格拆分为子网格。
1.通过材质定义将给定场景中的所有网格拆分为子网格。
1.通过材料定义将给定的网格拆分为子网格。
- **在类Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem** 
-它允许用户在导入或导出期间翻转U3D的坐标系。

开发人员可能要求按材料自动分割网格，以便每个网格仅使用一种材料或通过指定材料分割网格。这些帮助主题说明了如何做到这一点:[通过指定材质来分割网格](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)和[每个素材分割场景的所有网格](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **删除Distreet3DS格式。**
由于拼写不正确，Distreet3DS格式被标记为过时。
### **添加Discreet3DS格式。**
已经引入了Discreet3DS格式。
### **在类Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem**
它允许用户在导入或导出期间翻转U3D的坐标系。
