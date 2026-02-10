---
title: Générer des UV
type: docs
weight: 12
url: /fr/net/generate-uv/
description: Aspose.3D for .NET offre la classe PolygonModifier qui expose la méthode GenerateUV, avec laquelle vous pouvez générer manuellement UV et l'associer au maillage. L'extrait de code suivant montre la fonctionnalité complète pour le générer et l'associer.
---
#  **Générer des UV**
Aspose.3D for .NET propose une classe `PolygonModifier` qui expose la méthode `GenerateUV`, avec laquelle vous pouvez générer manuellement UV et l'associer au maillage. L'extrait de code suivant montre la fonctionnalité complète pour le générer et l'associer:



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
