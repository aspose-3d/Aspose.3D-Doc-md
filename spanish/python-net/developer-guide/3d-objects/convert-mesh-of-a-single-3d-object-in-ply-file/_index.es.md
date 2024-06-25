---
title: Convertir la malla de un solo objeto 3D en un archivo PLY
type: docs
weight: 20
url: /es/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Los miembros sobrecargados de EncodeMesh expuestos por la clase de PlyFormat se pueden utilizar para convertir la malla de un objeto 3D a un archivo PLY. Los miembros de EncodeMesh toman la malla, el nombre del archivo de salida y los objetos de PlySaveOptions como parámetros. Con las opciones de guardado de PLY, los desarrolladores pueden cambiar el nombre de los componentes de coordenadas.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API permite a los desarrolladores convertir la malla de un solo objeto 3D en el archivo PLY.

{{% /alert %}}
##  **Crear un objeto 3D y guardarlo en un archivo PLY**
Los miembros `encodeMesh` sobrecargados expuestos por la clase `PlyFormat` se pueden usar para convertir la malla de un objeto 3D en un archivo PLY. Los miembros `encodeMesh` toman como parámetros los objetos `Mesh`, nombre de archivo de salida y `PlySaveOptions`. Con las opciones de guardado de PLY, los desarrolladores pueden cambiar el nombre de los componentes de coordenadas.
###  **Muestra de programación**
En este ejemplo de código se crea un objeto 3D Cylinder y, a continuación, se codifica en el archivo PLY.

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
