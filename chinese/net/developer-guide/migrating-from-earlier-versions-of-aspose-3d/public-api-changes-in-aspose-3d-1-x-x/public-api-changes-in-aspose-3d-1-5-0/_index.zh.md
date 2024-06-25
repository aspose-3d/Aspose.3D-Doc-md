---
title: Aspose 中的公共 API 更改。3D 1.5.0
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-1-5-0/
---
**内容摘要**

- [将图元转换为网格并从图元 3D 模型创建场景](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [使用顶点的自定义内存布局将网格转换为三角形网格](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [分割网格](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [删除Distreet3DS格式。](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [添加 Discreet3DS 格式。](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [在类 Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本1.4.0到1.5.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **将图元转换为网格并从图元 3D 模型创建场景**
**添加了各种类、方法和属性**

- **添加接口 Aspose.ThreeD.Entities.IMeshConvertible。** 
-在导出为任何 3D 文件格式时，实现此接口的任何类都可以转换为网格。
- **添加类 Aspose.ThreeD.Entities.Primitive。** 
-它是从实体类派生的，也是所有原始类的基类。
- **添加类 Aspose.ThreeD.Entities.Box/Cylinder/Plane/Sphere/Torus。** 
-这些可以用来用简单原语定义场景。开发人员还可以将它们自动转换为网格。

图元包括许多最基本和最常用的对象，如长方体、球体、平面、圆柱体和圆环。开发人员还可以将它们转换为网格以进行修改。以下帮助主题说明了如何执行此操作: [将图元转换为网格](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) 和 [将图元转换为网格](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **使用顶点的自定义内存布局将网格转换为三角形网格**
**添加了各种类、方法和属性**

- **添加类 Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
-特里梅什/特里梅什<T>包含具有自定义内存布局的基于三角形的网格的定义，当开发人员要求将场景转换为自己的专有文件格式或渲染时，这很有用。
- **添加结构 Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
-这些类在float中呈现向量分量。只有少数现代GPU支持双精度矢量，单精度浮点类型在实时渲染世界中更受欢迎。这些替换将与原始Vector2/Vector3/Vector4共存，因为它们在 Aspose.3D 中扮演不同的角色。双精度主要用于存储模型的数据，因为它具有较少的累积误差。单精度主要用于渲染或用户自己的专有文件格式转换，因为它具有更好的接受度和性能。我们在 Aspose.3D 1.5中引入了这组向量，因为我们添加了对自定义顶点布局的支持，其中将经常使用浮点向量。
- **添加属性类 Aspose.ThreeD.Utilities.SemanticAttribute** 
-开发人员可以为vertex定义自定义结构，并使用此属性标记字段的语义。
- **添加类 Aspose.ThreeD.Utilities.Vertexdecaration** 
-它描述了顶点的内存布局。
- **添加枚举 Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
-这些枚举类型分别注释顶点字段的数据类型和语义。
- **添加类 Aspose.ThreeD.Utilities.VertexField** 
-它描述了Vertex的自定义内存布局中的每个字段。
- **添加类 Aspose.ThreeD.Utilities.Vertex** 
-可用于访问TriMesh/TriMesh中的原始顶点<T>

开发人员可以使用顶点的自定义内存布局将任何网格对象转换为三角形网格。图形软件包和硬件设备在三角形上更有效地运行。此帮助主题说明了如何执行此操作: [使用顶点的自定义内存布局将网格转换为三角形网格](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **分割网格**
**添加了各种类、方法和属性**

- **添加枚举 Aspose.ThreeD.Entities.SplitMeshPolicy** 
-它指定了网格分割算法中使用的数据策略，我们支持两种策略，在子网格之间共享数据或每个子网格都有自己的数据 (仅使用的数据)。
- **将3个SplitMesh方法添加到 Aspose.ThreeD.Entities.PolygonModifier类** 
1.通过材质定义将指定节点上的网格拆分为子网格。
1.通过材质定义将给定场景中的所有网格拆分为子网格。
1.通过材料定义将给定的网格拆分为子网格。
- **在类 Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem** 
-它允许用户在导入或导出期间翻转 U3D 的坐标系。

开发人员可能需要按材质自动拆分网格，以便每个网格仅使用一种材质或通过指定材质来拆分网格。以下帮助主题说明了如何执行此操作: [通过指定材质来分割网格](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) 和 [每个素材分割场景的所有网格](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **删除Distreet3DS格式。**
由于拼写不正确，Distreet3DS格式被标记为过时。
###  **添加 Discreet3DS 格式。**
已引入 Discreet3DS 格式。
###  **在类 Aspose.ThreeD.Formats.Universal3DConfig中添加属性FlipCoordinateSystem**
它允许用户在导入或导出期间翻转 U3D 的坐标系。
