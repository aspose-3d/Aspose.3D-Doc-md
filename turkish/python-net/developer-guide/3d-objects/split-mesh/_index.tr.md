---
title: Split Mesh
type: docs
weight: 100
url: /tr/python-net/split-mesh/
description: Geliştiriciler, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese ayırmayı gerektirebilir. Tek bir malzemeye atanmışsa, splitmesh yöntemi sahnenin bir ağını bölmez. Geliştiriciler şimdi Aspose.3D for Python via .NET API kullanarak bunu başarabilirler.
---
##  **Split All erial eshes bir cene cene er erial aterial**
Developers may require to split all meshes of a scene into several sub meshes per material. The `split_mesh` method will not split a mesh of the scene If it has been assigned a single material. Developers can now achieve this by using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}}

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

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
##  **Erial plit a erial esh erial pecicithe erial aterial**
Aspose.3D for Python via .NET API, geliştiricilerin malzemeyi manuel olarak belirterek bir ağı ayırmasına izin verir. Bölünmüş örgü seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
###  **Bplit Box Mesh**
Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](/3d/tr/python-net/create-3d-mesh-and-scene/). Ayrıca, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. Aşağıdaki kod örneği, malzemeyi manuel olarak belirterek ilkel bir ağ oluşturur.

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
