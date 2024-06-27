---
title: العمل بصيغة VRML
type: docs
weight: 90
url: /ar/nodejs-java/working-with-vrml-format/
description: يسمح Aspose.3D for Node.js via Java بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف VRML إلى فئة تنسيق الملفات. Aspose.3D يمكنه الكشف تلقائيًا عن تنسيق VRML ، لذلك عادة ما يتم تجاهل تنسيق الملف في طريقة مفتوحة.
---
#  **افتح تنسيق ملف VRML**
يسمح Aspose.3D for Node.js via Java بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف `VRML` إلى فئة `FileFormat`. Aspose.3D يمكنه الكشف تلقائيًا عن تنسيق `VRML` ، لذلك عادة ما يتم تجاهل `FileFormat` في طريقة مفتوحة. يوضح مقتطف الشفرة التالي كيفية فتح تنسيق ملف VRML.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
