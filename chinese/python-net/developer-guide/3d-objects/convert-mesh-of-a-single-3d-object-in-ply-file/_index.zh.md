---
title: 转换 PLY 文件中单个 3D 对象的网格
type: docs
weight: 20
url: /zh/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: 由PlyFormat类公开的重载EncodeMesh成员可用于将 3D 对象的网格转换为 PLY 文件。EncodeMesh成员将网格、输出文件名和PlySaveOptions对象作为参数。使用 PLY 保存选项，开发人员可以更改坐标组件的名称。
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API 允许开发人员转换 PLY 文件中单个 3D 对象的网格。

{{% /alert %}}
##  **创建 3D 对象并将其保存到 PLY 文件**
`PlyFormat` 类公开的重载 `encodeMesh` 成员可用于将 3D 对象的网格转换为 PLY 文件。`encodeMesh` 成员将 `Mesh` 、输出文件名和 `PlySaveOptions` 对象作为参数。使用 PLY 保存选项，开发人员可以更改坐标组件的名称。
###  **编程示例**
此代码示例创建一个 3D Cylinder对象，然后在 PLY 文件中进行编码。

**Python**

```py

from aspose.threed import FileFormat, FileContentType
from aspose.threed.entities import Cylinder
from aspose.threed.formats import PlySaveOptions

# Create a cylinder object and save it to ply file

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply")

# using Ply save options

# Save as binary PLY format, the default value is ASCII

opt = PlySaveOptions(FileContentType.BINARY)

# change the components to 's' and 't'

opt.texture_coordinate_components.item1 = "s
opt.texture_coordinate_components.item2 = "t"

# save the mesh

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply", opt)

```
