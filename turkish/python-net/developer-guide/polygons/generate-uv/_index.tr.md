---
title: Enerenerate UV
type: docs
weight: 20
url: /tr/python-net/generate-uv/
description: Aspose.3D for Python via .NET, uv'yi manuel olarak üretebileceğiniz ve ağ ile ilişkilendirebileceğiniz generateuv yöntemini ortaya koyan poligondeğiştirici sınıfı sunar. Kod parçacığının ardından, oluşturmak ve ilişkilendirmek için tam işlevsellik gösterir.
---
#  **Enerenerate UV**
Aspose.3D for Python via .NET, uv'yi manuel olarak oluşturabileceğiniz ve ağ ile ilişkilendirebileceğiniz `generate_uv` yöntemini ortaya koyan `PolygonModifier` sınıfı sunar. Aşağıdaki kod parçacığı, oluşturmak ve ilişkilendirmek için tam işlevselliği gösterir:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, PolygonModifier, VertexElementType

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
scene = Scene()
# since all primitive entities in Aspose.3D will have builtin UV generation
# here we manually remove it to assume we have a mesh without UV data
mesh = Box().to_mesh()
mesh.vertex_elements.remove(mesh.get_element(VertexElementType.UV))
# then we can manually generate UV for it
uv = PolygonModifier.generate_uv(mesh)
# generated UV data is not associated with the mesh, we should manually do this
mesh.add_element(uv)
# put it to the scene
node = scene.root_node.create_child_node(mesh)
# then save it
scene.save("out"  + "Aspose.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
