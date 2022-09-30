---
title: Convert esh esh من كائن واحد 3D في ملف PLY
type: docs
weight: 20
url: /ar/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Tانه تحميل الزائد أعضاء EncodeMsh يتعرض من قبل فئة lylyFormat يمكن استخدامها لتحويل esh esh من كائن 3D إلى ملف PLY. The Eأعضاء ncodeMsh تأخذ Mesh ، اسم ملف الإخراج والأشياء ptions lySaveOكما المعلمات. Uالغناء PLY حفظ الخيارات ، يمكن للمطورين تغيير اسم مكونات التنسيق.
---
{{% alert color="primary" %}}

[Aspose.3D ل Python via .NET](https://products.aspose.com/3d/python-net/)API يسمح للمطورين لتحويل esh esh من كائن واحد 3D في ملف PLY.

{{% /alert %}}
## **Rereate كائن 3D وحفظه إلى ملف PLY**
Tانه فوق تحميل `encodeMesh` أعضاء يتعرض من قبل فئة `PlyFormat` يمكن استخدامها لتحويل esh sh من كائن 3D إلى ملف PLY. The `encodeMesh` أعضاء تأخذ `Mesh` ، اسم ملف الإخراج و `PlySaveOptions` الكائنات كمعلمات. Uالغناء PLY حفظ الخيارات ، يمكن للمطورين تغيير اسم مكونات التنسيق.
### **Pروغرامينغ ple وافرة**
Tمثال التعليمات البرمجية له يخلق كائن ylinder 3D C، ثم ترميز في ملف PLY.

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
