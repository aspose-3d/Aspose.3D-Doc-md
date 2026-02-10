---
title: Geteiltes Netz
type: docs
weight: 100
url: /de/net/split-mesh/
description: Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie Aspose.3D for .NET API verwenden.
---
##  **Alle Maschen einer Szene pro Material aufteilen**
Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API verwenden.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Es unterstützt zwei Richtlinien, Daten zwischen Subnetz teilen oder jedes Sub-Mesh hat seine eigenen Daten (nur verwendete Daten).

{{% /alert %}}

Das folgende Code beispiel teilt alle Maschen einer Szene pro Material auf. Jedes Teil netz teilt die gleichen direkten Daten und unter scheidet sich nur in Indizes.

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
##  **Teilen Sie ein Netz, indem Sie das Material angeben**
Aspose.3D for .NET API ermöglicht es Entwicklern, ein Netz aufzuteilen, indem sie das Material manuell angeben. Die Split-Mesh-Option erstellt separate Objekte und jedes Sub-Mesh verwendet nur ein Material.
###  **Teilen Sie das Netz der Box**
Dieses Hilfe thema erstellt ein Netz der Box, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [Erstellen Sie ein 3D Cube Mesh](/3d/de/net/create-3d-mesh-and-scene/). Darüber hinaus besteht eine Box aus 6 Ebenen und jede Ebene wird zu einem Teilnetz. Das folgende Code beispiel teilt ein primitives Netz, indem das Material manuell angegeben wird.

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
