---
title: Convert Mesh of a single 3D object in PLY file
type: docs
weight: 20
url: /python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: The overloaded EncodeMesh members exposed by the PlyFormat class can be used to convert the Mesh of a 3D object to PLY file. The EncodeMesh members take the Mesh, output file name and PlySaveOptions objects as parameters. Using the PLY save options, developers can change the name of coordinate components.
---

{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to convert the Mesh of a single 3D object in the PLY file.

{{% /alert %}}
## **Create a 3D object and save it to PLY file**
The overloaded `encodeMesh` members exposed by the `PlyFormat` class can be used to convert the Mesh of a 3D object to PLY file. The `encodeMesh` members take the `Mesh`, output file name and `PlySaveOptions` objects as parameters. Using the PLY save options, developers can change the name of coordinate components.
### **Programming Sample**
This code example creates a 3D Cylinder object, and then encode in the PLY file.

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
