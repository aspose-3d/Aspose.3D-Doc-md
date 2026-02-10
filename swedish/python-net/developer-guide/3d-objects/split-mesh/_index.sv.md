---
title: Dela mask
type: docs
weight: 100
url: /sv/python-net/split-mesh/
description: Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda Aspose.3D for Python via .NET API.
---
##  **Dela alla masker av en scen per material**
Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. `split_mesh`-metoden delar inte en mask på scenen om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum anger datapolicyn som används i algoritmen för uppdelning av mesh. Den stöder två regler. dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}}

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import PolygonModifier, SplitMeshPolicy

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
input = "data-dir"  + "test.fbx"
#  Load a 3D file
scene = Scene(input)
#  Split all meshes
PolygonModifier.split_mesh(scene, SplitMeshPolicy.CLONE_DATA)
#  Save file
output = "out"  + "test-splitted.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Dela ett mask genom att ange materialet**
Aspose.3D for Python via .NET API tillåter utvecklare att dela en mesh genom att manuellt ange materialet. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
###  **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa en 3D kubst](/3d/sv/python-net/create-3d-mesh-and-scene/). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera materialet.

{{< highlight "python" >}}
from aspose import pycore
from aspose.threed.entities import Box, MappingMode, PolygonModifier, ReferenceMode, SplitMeshPolicy, VertexElementMaterial, VertexElementType

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a mesh of box(A box is composed by 6 planes)
box = Box().to_mesh()
#  Create a material element on this mesh
mat = pycore.cast(VertexElementMaterial, box.create_element(VertexElementType.MATERIAL, MappingMode.POLYGON, ReferenceMode.INDEX))
#  And specify different material index for each plane
mat.indices.extend([0, 1, 2, 3, 4, 5 ])
#  Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
#  We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
planes = PolygonModifier.split_mesh(box, SplitMeshPolicy.CLONE_DATA)
mat.indices.clear()
mat.indices.extend([0, 0, 0, 1, 1, 1 ])
#  Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
#  We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
planes = PolygonModifier.split_mesh(box, SplitMeshPolicy.COMPACT_DATA)

{{< /highlight >}}
