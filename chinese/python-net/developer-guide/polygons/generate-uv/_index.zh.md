---
title: 产生紫外线
type: docs
weight: 20
url: /zh/python-net/generate-uv/
description: Aspose.3D for Python via .NET 提供了公开GenerateUV方法的PolygonModifier类，您可以使用该方法手动生成UV并将其与网格关联。下面的代码片段显示了生成和关联它的完整功能。
---
#  **产生紫外线**
Aspose.3D for Python via .NET 提供了 `PolygonModifier` 类，该类公开了 `generate_uv` 方法，您可以使用该方法手动生成UV并将其与网格关联。以下代码段显示了生成和关联它的完整功能:



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
