---
title: MappingMode和ReferenceMode说明
type: docs
weight: 10
url: /zh/net/mapping-mode-and-reference-mode-explains
description: 使用 Aspose.3D for .NET，开发人员可以定义具有各种顶点数据元素的网格，这里我们解释如何将数据映射到网格的组件并恢复数据。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员可以定义具有各种顶点数据元素的网格，包括法线、颜色和权重。Aspose.3D 提供两种优化数据重用的机制: `MappingMode` 和 `ReferenceMode`。这些机制旨在最小化网格的内存占用，特别是在 FBX 和 USD 等高级格式中。MappingMode允许将顶点数据高效映射到网格组件，而ReferenceMode便于跨多个网格组件引用顶点元素数据。这些功能共同提高了性能和内存效率，使 Aspose.3D 成为在 .NET 应用程序中处理复杂 3D 模型的强大工具。

{{% /alert %}}



###  `MappingMode` 解释

 `MappingMode` 确定元素数据如何映射到 Aspose.3D for .NET 中几何图形的曲面。它提供了多种定义此映射的方法:

1. **控制点**,每个数据元素都映射到几何图形的控制点。此模式可确保定义几何图形形状的每个控制点与特定数据元素相关联。
1. **多边形顶点**,数据被映射到一个多边形的顶点。在控制点由多个多边形共享的情况下，控制点的每个实例在其出现在不同的多边形中时将具有其自己的不同数据。这确保了当它们用作不同多边形的顶点时，即使共享的控制点也可以具有唯一的数据。
1. **多边形**,数据被映射到整个多边形。这意味着多边形的所有顶点共享相同的数据元素。当需要在整个多边形曲面上应用统一数据时，此模式非常有用，可确保多边形内的一致性。
1. **边缘**,数据被映射到几何图形的边缘。边的每个端点共享相同的数据，从而提供了一种将统一数据应用于边同时允许不同边的不同数据的方式。这对于定义特定于边的特性 (如折痕值或基于边的属性) 特别有用
1. **全部相同**,单个数据元素将映射到几何图形的整个表面。无论数据是被解释为控制点、多边形顶点还是边端点，相同的数据值将统一应用于所有元素。此模式非常适合需要在整个几何图形中保持常量值的情况，以确保在整个 3D 模型中具有统一的属性。




###  `ReferenceMode` 解释
 `ReferenceMode` 定义是否按索引重用数据，`ReferenceMode` 有三个策略:

1.**直接**,数据被直接引用，并存储在 `VertexElement` 的 `Data` 属性中。
1.**IndexToDirect**,数据由索引引用，然后在 `VertexElement` 的数据列表中按索引访问。
1.**索引**,数据仅由索引引用，现在只有 `VertexElementMaterial` 使用此引用模式，这类似于 `IndexToDirect`，但不同之处在于材料是在 `Node` 的属性 `Materials` 下定义的，而不是在 `VertexElementMaterial` 中定义的，所有 `VertexElement` 仅适用于原始数据。



例如，给定多维数据集的定义:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

如果要将红色分配给控制点0和1，将绿色分配给控制点2和3，将蓝色分配给控制点4和5，将白色分配给控制点6和7，则可以使用以下方法实现此目的:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

若要有效地将颜色分配给控制点并减少内存消耗，可以使用索引来引用颜色。通过分别定义颜色，然后使用索引引用它们，可以最大程度地减少冗余。这里是你如何实现这一点:

首先，在Vector4类型中为唯一颜色定义4种颜色，然后使用8个索引的数组将这些颜色分配给每个控制点:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

在这种方法中:

1. 定义唯一的颜色: 只有4种颜色 (红色，绿色，蓝色，白色) 定义为Vector4实例。
1. 创建颜色索引数组: 使用8个索引的数组来引用每个控制点的这4种颜色。
1. 使用索引映射颜色: 通过索引引用颜色，可以减少内存消耗，因为每种颜色都存储一次并在多个控制点之间重复使用。

此方法通过减少冗余数据存储来优化内存使用，从而提高 3D 模型的效率。