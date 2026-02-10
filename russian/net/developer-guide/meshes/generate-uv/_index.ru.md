---
title: Генерировать УФ
type: docs
weight: 12
url: /ru/net/generate-uv/
description: Aspose.3D for .NET предлагает класс PolygonModifier, который предоставляет метод GenerateUV, с помощью которого вы можете вручную генерировать UV и связывать его с сеткой. Следующий фрагмент кода показывает полную функциональность для его генерации и связывания.
---
#  **Генерировать УФ**
Aspose.3D for .NET предлагает класс `PolygonModifier`, который предоставляет метод `GenerateUV`, с помощью которого вы можете вручную сгенерировать УФ и связать его с сеткой. Следующий фрагмент кода показывает полную функциональность для его генерации и связывания:



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
