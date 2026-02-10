---
title: Generare UV
type: docs
weight: 12
url: /it/net/generate-uv/
description: Aspose.3D for .NET offre la classe PolygonModifier che espone il metodo GenerateUV, con il quale è possibile generare manualmente UV e associarlo alla mesh. Il seguente frammento di codice mostra la funzionalità completa per generarlo e associarlo.
---
#  **Generare UV**
Aspose.3D for .NET offre una classe `PolygonModifier` che espone il metodo `GenerateUV`, con il quale è possibile generare manualmente UV e associarlo alla mesh. Il seguente frammento di codice mostra la funzionalità completa per generarlo e associarlo:



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
