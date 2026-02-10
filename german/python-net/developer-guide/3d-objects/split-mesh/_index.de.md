---
title: Geteiltes Netz
type: docs
weight: 100
url: /de/python-net/split-mesh/
description: Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie Aspose.3D for Python via .NET API verwenden.
---
##  **Alle Maschen einer Szene pro Material aufteilen**
Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die `split_mesh`-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API verwenden.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Es unterstützt zwei Richtlinien, Daten zwischen Subnetz teilen oder jedes Sub-Mesh hat seine eigenen Daten (nur verwendete Daten).

{{% /alert %}}

Das folgende Code beispiel teilt alle Maschen einer Szene pro Material auf. Jedes Teil netz teilt die gleichen direkten Daten und unter scheidet sich nur in Indizes.

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
##  **Teilen Sie ein Netz, indem Sie das Material angeben**
Mit Aspose.3D for Python via .NET API können Entwickler ein Netz aufteilen, indem sie das Material manuell angeben. Die Split-Mesh-Option erstellt separate Objekte und jedes Sub-Mesh verwendet nur ein Material.
###  **Teilen Sie das Netz der Box**
Dieses Hilfe thema erstellt ein Netz der Box, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [Erstellen Sie ein 3D Cube Mesh](/3d/de/python-net/create-3d-mesh-and-scene/). Darüber hinaus besteht eine Box aus 6 Ebenen und jede Ebene wird zu einem Teilnetz. Das folgende Code beispiel teilt ein primitives Netz, indem das Material manuell angegeben wird.

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
