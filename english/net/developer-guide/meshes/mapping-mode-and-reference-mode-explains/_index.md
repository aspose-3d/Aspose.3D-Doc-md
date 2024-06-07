---
title: MappingMode and ReferenceMode explains
type: docs
weight: 10
url: /net/mapping-mode-and-reference-mode-explains
description: Using Aspose.3D for .NET, developers can define mesh with various vertex data elements, here we explain how to map data to meshes' component and resuze data.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can define meshes with various vertex data elements, including normals, colors, and weights. Aspose.3D offers two mechanisms to optimize data reuse: `MappingMode` and `ReferenceMode`. These mechanisms are designed to minimize the memory footprint of meshes, particularly in advanced formats like FBX and USD. MappingMode allows for efficient mapping of vertex data to mesh components, while ReferenceMode facilitates the referencing of vertex element data across multiple mesh components. Together, these features enhance performance and memory efficiency, making Aspose.3D a powerful tool for handling complex 3D models in .NET applications.

{{% /alert %}}



### `MappingMode` explains

 `MappingMode` determines how the element data is mapped to the surface of the geometry in Aspose.3D for .NET. It provides various ways to define this mapping:

1. **ControlPoint**,  Each data element is mapped to the control point of the geometry. This mode ensures that each control point, which defines the shape of the geometry, is associated with a specific data element.
1. **PolygonVertex**, The data is mapped to the vertex of a polygon. In cases where a control point is shared by multiple polygons, each instance of the control point, as it appears in different polygons, will have its own distinct data. This ensures that even shared control points can have unique data when they serve as vertices for different polygons.
1. **Polygon**, The data is mapped to the entire polygon. This means that all vertices of a polygon share the same data element. This mode is useful when uniform data needs to be applied across the entire polygon surface, ensuring consistency within the polygon.
1. **Edge**, The data is mapped to the edges of the geometry. Each endpoint of an edge shares the same data, providing a way to apply uniform data to the edges while allowing distinct data for different edges. This can be particularly useful for defining characteristics that are specific to edges, such as crease values or edge-based attributes
1. **AllSame**, A single data element is mapped to the entire surface of the geometry. Regardless of whether the data is interpreted as control points, polygon vertices, or edge endpoints, the same data value is applied uniformly across all elements. This mode is ideal for scenarios where a constant value needs to be maintained throughout the entire geometry, ensuring a uniform attribute across the entire 3D model.




### `ReferenceMode` explains
 `ReferenceMode` defines whether to reuse data by indices, there's three policies for `ReferenceMode`:

 1.  **Direct**, data is directly referenced, and stored in `VertexElement`'s `Data` property.
 1.  **IndexToDirect**, the data is referenced by index, then accessed by index in `VertexElement`'s data list.
 1.  **Index**, data is only referenced by index, now only the `VertexElementMaterial` use this reference mode, this is similar to `IndexToDirect` but the differences is the materials are defined under the `Node`'s property `Materials`, not in the `VertexElementMaterial`, all `VertexElement` only works with primitive data.



For example, given a definition of a cube:

{{< highlight csharp >}}
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

If you want to assign red to control points 0 and 1, green to control points 2 and 3, blue to control points 4 and 5, and white to control points 6 and 7, you can achieve this with the following approach:

{{< highlight csharp >}}
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

To assign colors to control points efficiently and reduce memory consumption, you can use indices to reference the colors. By defining the colors separately and then referencing them with indices, you can minimize redundancy. Here’s how you can achieve this:

First, define 4 colors in the Vector4 type for the unique colors, and then use an array of 8 indices to assign these colors to each control point:

{{< highlight csharp >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

In this approach:

1.    Define unique colors: Only 4 colors are defined (red, green, blue, white) as Vector4 instances.
1.    Create a color index array: An array of 8 indices is used to reference these 4 colors for each control point.
1.    Map colors using indices: By referencing the colors through indices, you reduce the memory consumption, as each color is stored once and reused across multiple control points.

This method optimizes memory usage by reducing redundant data storage, making your 3D model more efficient.