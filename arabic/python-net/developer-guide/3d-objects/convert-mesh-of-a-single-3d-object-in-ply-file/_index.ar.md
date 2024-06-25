---
title: تحويل شبكة لكائن واحد 3D في ملف PLY
type: docs
weight: 20
url: /ar/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: يمكن استخدام أعضاء EncodeMesh الذين تم تعريضهم من قبل فئة plysformat لتحويل شبكة اعتراض 3D إلى ملف PLY. يأخذ أعضاء EncodeMesh الشبكة ، اسم ملف الإخراج وكائنات PlySaveOptions كمعاملات. باستخدام خيارات الحفظ PLY ، يمكن للمطورين تغيير اسم مكونات الإحداثيات.
---
{{% alert color="primary" %}}

يسمح [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API للمطورين بتحويل شبكة كائن 3D واحد في ملف PLY.

{{% /alert %}}
##  **إنشاء كائن 3D وحفظه في ملف PLY**
يمكن استخدام أعضاء `encodeMesh` الذين تم تعريضهم بواسطة فئة `PlyFormat` لزيادة التحميل لتحويل اعتراض شبكة 3D إلى ملف PLY. يأخذ أعضاء `encodeMesh` `Mesh` واسم ملف الإخراج وكائنات `PlySaveOptions` كمعلمات. باستخدام خيارات الحفظ PLY ، يمكن للمطورين تغيير اسم مكونات الإحداثيات.
###  **Pروغرامينغ ple وافرة**
يُنشئ مثال الرمز هذا كائن أسطواني 3D ، ثم يُشفر في ملف PLY.

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
