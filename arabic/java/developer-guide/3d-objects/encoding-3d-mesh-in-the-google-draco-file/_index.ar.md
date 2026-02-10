---
title: ترميز 3D شبكة في ملف Google Draco
type: docs
weight: 30
url: /ar/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API يدعم استيراد طراز 3D ، واسترداد الشبكة ، ثم ترميز الشبكة في ملف Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API يدعم استيراد طراز 3D ، واسترداد الشبكة ، ثم ترميز الشبكة في ملف Google Draco. يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.

{{% /alert %}} 
##  **استرجع شبكة 3D وشفّر في ملف Google Draco**
يمكن استخدام طريقة الترميز التي تعرضها فئة `DracoFormat` لترميز شبكة 3D في ملف Google Draco. يتطلب الأمر وجود كائنات `Mesh` و `DracoSaveOptions` كمعلمات. مع خيارات الحفظ Draco ، يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.
###  **Pروغرامينغ ple وافرة**
هذا المثال البرمجي يسترد شبكة كروية ، ثم يتم ترميله في الملف Google Draco بعد تحديد مستوى الضغط.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
