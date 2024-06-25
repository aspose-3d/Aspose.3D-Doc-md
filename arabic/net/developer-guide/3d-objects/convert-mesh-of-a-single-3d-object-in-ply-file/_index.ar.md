---
title: تحويل شبكة لكائن واحد 3D في ملف PLY
type: docs
weight: 20
url: /ar/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: يمكن استخدام أعضاء EncodeMesh الذين تم تعريضهم من قبل فئة plysformat لتحويل شبكة اعتراض 3D إلى ملف PLY. يأخذ أعضاء EncodeMesh الشبكة ، اسم ملف الإخراج وكائنات PlySaveOptions كمعاملات. باستخدام خيارات الحفظ PLY ، يمكن للمطورين تغيير اسم مكونات الإحداثيات.
---
{{% alert color="primary" %}}

يسمح [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API للمطورين بتحويل شبكة كائن 3D واحد في ملف PLY.

{{% /alert %}}
##  **إنشاء كائن 3D وحفظه في ملف PLY**
يمكن استخدام أعضاء `EncodeMesh` الذين تم تعريضهم فوق طاتهم من فئة `PlyFormat` لتحويل `Mesh` من 3D إلى ملف PLY. يأخذ أعضاء `EncodeMesh` `Mesh` واسم ملف الإخراج وكائنات `PlySaveOptions` كمعلمات. باستخدام خيارات الحفظ PLY ، يمكن للمطورين تغيير اسم مكونات الإحداثيات.
###  **Pروغرامينغ ple وافرة**
يُنشئ مثال الرمز هذا كائن أسطواني 3D ، ثم يُشفر في ملف PLY.

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
