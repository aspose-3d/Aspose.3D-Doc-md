---
title: Dela mask
type: docs
weight: 100
url: /sv/net/split-mesh/
description: Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda Aspose.3D for .NET API.
---
##  **Dela alla masker av en scen per material**
Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum anger datapolicyn som används i algoritmen för uppdelning av mesh. Den stöder två regler. dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}}

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

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
##  **Dela ett mask genom att ange materialet**
Aspose.3D for .NET API tillåter utvecklare att dela en mask genom att manuellt ange materialet. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
###  **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa en 3D kubst](/3d/sv/net/create-3d-mesh-and-scene/). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera materialet.

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
