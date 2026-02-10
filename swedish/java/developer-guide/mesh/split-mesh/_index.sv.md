---
title: Dela mask
type: docs
weight: 10
url: /sv/java/split-mesh/
description: Aspose.3D for Java API har stöd för att dela alla maskor i en scen i flera delar per material. SplitMesh-metoden kommer inte att dela en mesh på scenen, om den har tilldelats ett enda material. Det kan uppnås genom att använda Aspose.3D for Java API.
---
##  **Dela alla masker av Scen per material.**
Aspose.3D for Java API har stöd för att dela alla maskor i en scen i flera delar per material. SplitMesh-metoden kommer inte att dela en mesh på scenen, om den har tilldelats ett enda material. Det kan uppnås genom att använda Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum anger datapolicyn som används i algoritmen för uppdelning av mesh. Den stöder två regler. dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}} 

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "test.fbx";
// Load a 3D file
Scene scene = new Scene(MyDir);
// Split all meshes
PolygonModifier.splitMesh(scene, SplitMeshPolicy.CLONE_DATA);
// Save file
MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("test-splitted.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Dela ett mask genom att ange materialet**
Aspose.3D for Java API har stöd för att dela en mask genom att materialet manuellt anges. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
###  **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa en 3D kubst](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera material.

{{< highlight "java" >}}
// Create a mesh of box(A box is composed by 6 planes)
Mesh box = (new Box()).toMesh();
// Create a material element on this mesh
VertexElementMaterial mat = (VertexElementMaterial) box.createElement(VertexElementType.MATERIAL, MappingMode.POLYGON, ReferenceMode.INDEX);
// and specify different material index for each plane
mat.setIndices(new int[]{0, 1, 2, 3, 4, 5});
// Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
// We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
Mesh[] planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.CLONE_DATA);
mat.getIndices().clear();
mat.setIndices(new int[]{0, 0, 0, 1, 1, 1});
// Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
// We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.COMPACT_DATA);
{{< /highlight >}}
