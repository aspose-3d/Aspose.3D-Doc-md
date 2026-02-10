---
title: العمل بصيغة VRML
type: docs
weight: 90
url: /ar/java/working-with-vrml-format/
description: Aspose.3D for Java يسمح بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف VRML إلى فئة تنسيق الملفات. Aspose.3D يمكنه الكشف تلقائيًا عن تنسيق VRML ، لذلك عادة ما يتم تجاهل تنسيق الملفات في طريقة مفتوحة.
---
#  **افتح تنسيق ملف VRML**
Aspose.3D for Java يسمح بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف `VRML` إلى فئة `FileFormat`. Aspose.3D يمكنه الكشف تلقائيًا عن تنسيق `VRML` ، لذلك عادة ما يتم تجاهل `FileFormat` في طريقة مفتوحة. يوضح مقتطف الشفرة التالي كيفية فتح تنسيق ملف VRML.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// open Virtual Reality Modeling Language (VRML) file format
scene.open( MyDir + "test.wrl");
// work with VRML file format...

{{< /highlight >}}
