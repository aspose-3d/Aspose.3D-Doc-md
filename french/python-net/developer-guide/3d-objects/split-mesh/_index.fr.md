---
title: Maille fendue
type: docs
weight: 100
url: /fr/python-net/split-mesh/
description: Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant Aspose.3D for Python via .NET API.
---
##  **Divisez tous les mailles d'une scène par matériau**
Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode `split_mesh` ne divisera pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de division de maillage, il prend en charge deux politiques, partage de données entre sous-maillages ou chaque sous-maillage a ses propres données (uniquement des données utilisées).

{{% /alert %}}

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

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
##  **Diviser un maillage en spécifiant le matériau**
Aspose.3D for Python via .NET API permet aux développeurs de diviser un maillage en spécifiant manuellement le matériau. L'option de maillage fractionné crée des objets séparés et chaque sous maillage utilisera un seul matériau.
###  **Fendre la maille de la boîte**
Cette rubrique d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](/3d/fr/python-net/create-3d-mesh-and-scene/). En outre, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'exemple de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

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
