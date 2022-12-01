---
title: Convert esh esh من كائن واحد 3D في ملف PLY
type: docs
weight: 20
url: /ar/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Tانه تحميل الزائد أعضاء EncodeMsh يتعرض من قبل فئة lylyFormat يمكن استخدامها لتحويل esh esh من كائن 3D إلى ملف PLY. The Eأعضاء ncodeMsh تأخذ Mesh ، اسم ملف الإخراج والأشياء ptions lySaveOكما المعلمات. Uالغناء PLY حفظ الخيارات ، يمكن للمطورين تغيير اسم مكونات التنسيق.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API يسمح للمطورين لتحويل esh esh من كائن واحد 3D في ملف PLY.

{{% /alert %}}
## **Rereate كائن 3D وحفظه إلى ملف PLY**
Tانه فوق تحميل `EncodeMesh` أعضاء يتعرض من قبل فئة `PlyFormat` يمكن استخدامها لتحويل `Mesh` من كائن 3D إلى ملف PLY. The `EncodeMesh` أعضاء تأخذ `Mesh` ، اسم ملف الإخراج و `PlySaveOptions` الكائنات كمعلمات. Uالغناء PLY حفظ الخيارات ، يمكن للمطورين تغيير اسم مكونات التنسيق.
### **Pروغرامينغ ple وافرة**
Tمثال التعليمات البرمجية له يخلق كائن ylinder 3D C، ثم ترميز في ملف PLY.

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
