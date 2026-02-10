---
title: Malla dividida
type: docs
weight: 100
url: /es/python-net/split-mesh/
description: Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando Aspose.3D for Python via .NET API.
---
##  **Dividir todas las mallas de una escena por material**
Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método `split_mesh` no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre submallas o cada submalla tiene sus propios datos (solo datos utilizados).

{{% /alert %}}

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

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
##  **Dividir una malla especificando el material**
Aspose.3D for Python via .NET API permite a los desarrolladores dividir una malla especificando manualmente el material. La opción de dividir malla crea objetos separados y cada submalla utilizará un solo material.
###  **Dividir la malla de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](/3d/es/python-net/create-3d-mesh-and-scene/). Además, una caja está compuesta por 6 planos y cada plano se convertirá en una sub-malla. El ejemplo de código siguiente divide una malla primitiva especificando manualmente el material.

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
