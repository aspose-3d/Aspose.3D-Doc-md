---
title: Construir datos tangentes y binormales para todas las mallas en el modelo 3D
type: docs
weight: 30
url: /es/net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden crear datos tangentes y binormales para todas las mallas en cualquier archivo 3D compatible.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, los desarrolladores pueden construir datos tangentes y binormales para todas las mallas en cualquier archivo 3D compatible.

{{% /alert %}}
##  **Construir datos tangentes y binormales para malla**
Hemos agregado dos métodos BuildTangentBinormal en la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier). Un método toma el objeto de clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) como parámetro y otro toma el objeto de clase [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) como parámetro como se muestra en este ejemplo de código:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = new Scene(RunExamples.GetDataFilePath("document.fbx"));
// Triangulate a scene
PolygonModifier.BuildTangentBinormal(scene);
// Save 3D scene
scene.Save(RunExamples.GetOutputFilePath("BuildTangentAndBinormalData_out.fbx"), FileFormat.FBX7400ASCII);

{{< /highlight >}}
