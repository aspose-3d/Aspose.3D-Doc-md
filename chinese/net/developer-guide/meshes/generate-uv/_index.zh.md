---
title: 产生紫外线
type: docs
weight: 12
url: /zh/net/generate-uv/
description: Aspose.3D for .NET 提供了用于公开GenerateUV方法的PolygonModifier类，您可以使用该类手动生成UV并将其与网格关联。下面的代码片段显示了生成和关联它的完整功能。
---
#  **产生紫外线**
Aspose.3D for .NET 提供 `PolygonModifier` 类，该类公开 `GenerateUV` 方法，您可以使用该方法手动生成UV并将其与网格关联。以下代码段显示了生成和关联它的完整功能:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = new Scene();
//since all primitive entities in Aspose.3D will have builtin UV generation
//here we manually remove it to assume we have a mesh without UV data
var mesh = (new Box()).ToMesh();
mesh.VertexElements.Remove(mesh.GetElement(VertexElementType.UV));
//then we can manually generate UV for it
var uv = PolygonModifier.GenerateUV(mesh);
//generated UV data is not associated with the mesh, we should manually do this
mesh.AddElement(uv);
//put it to the scene
var node = scene.RootNode.CreateChildNode(mesh);
//then save it
scene.Save("Aspose.obj");

{{< /highlight >}}
