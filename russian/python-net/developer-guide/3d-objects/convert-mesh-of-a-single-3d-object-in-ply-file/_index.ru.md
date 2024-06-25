---
title: Преобразование Mesh одного объекта 3D в файл PLY
type: docs
weight: 20
url: /ru/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Для преобразования сетки объекта 3D в файл PLY можно использовать перегруженные члены EncodeMesh, выставленные классом PlyFormat. Члены EncodeMesh принимают в качестве параметров Mesh, имя выходного файла и объекты PlySaveOptions. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API позволяет разработчикам конвертировать сетку одного объекта 3D в файл PLY.

{{% /alert %}}
##  **Создайте объект 3D и сохраните его в файле PLY**
Для преобразования Mesh объекта 3D в файл PLY можно использовать перегруженные члены `encodeMesh`, выставленные классом `PlyFormat`. Участники `encodeMesh` принимают `Mesh`, имя выходного файла и объекты `PlySaveOptions` в качестве параметров. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
###  **Образец программирования**
Этот пример кода создает объект 3D Cylinder, а затем кодируют в файле PLY.

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
