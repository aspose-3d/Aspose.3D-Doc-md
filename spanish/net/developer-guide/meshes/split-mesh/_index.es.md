---
title: Malla dividida
type: docs
weight: 100
url: /es/net/split-mesh/
description: Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando Aspose.3D for .NET API.
---
##  **Dividir todas las mallas de una escena por material**
Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre submallas o cada submalla tiene sus propios datos (solo datos utilizados).

{{% /alert %}}

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
string input = RunExamples.GetDataFilePath("test.fbx");

// Load a 3D file
Scene scene = new Scene(input);
// Split all meshes
PolygonModifier.SplitMesh(scene, SplitMeshPolicy.CloneData);

// Save file
var output = RunExamples.GetOutputFilePath("test-splitted.fbx");
scene.Save(output, FileFormat.FBX7500ASCII);


{{< /highlight >}}
##  **Dividir una malla especificando el material**
Aspose.3D for .NET API permite a los desarrolladores dividir una malla especificando manualmente el material. La opción de dividir malla crea objetos separados y cada submalla utilizará un solo material.
###  **Dividir la malla de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](/3d/es/net/create-3d-mesh-and-scene/). Además, una caja está compuesta por 6 planos y cada plano se convertirá en una sub-malla. El ejemplo de código siguiente divide una malla primitiva especificando manualmente el material.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a mesh of box(A box is composed by 6 planes)
            Mesh box = (new Box()).ToMesh();
            // Create a material element on this mesh
            VertexElementMaterial mat = (VertexElementMaterial)box.CreateElement(VertexElementType.Material, MappingMode.Polygon, ReferenceMode.Index);
            // And specify different material index for each plane
            mat.Indices.AddRange(new int[] { 0, 1, 2, 3, 4, 5 });
            // Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
            // We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
            Mesh[] planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CloneData);

            mat.Indices.Clear();
            mat.Indices.AddRange(new int[] { 0, 0, 0, 1, 1, 1 });
            // Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
            // We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
            planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CompactData);


{{< /highlight >}}
