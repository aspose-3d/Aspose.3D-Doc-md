---
title: تصدير الملفات الملمس مع توفير 3D مشهد
type: docs
weight: 10
url: /ar/net/export-texture-files-while-saving-3d-scene
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين تصدير ملفات نسيجية إلى نظام الملفات مع توفير مشهد 3D.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، عند تصدير مشهد إلى ملفات ، من الضروري في كثير من الأحيان تصدير التركيبات ، سواء المضمنة أو الخارجية ، إلى الدليل نفسه. Aspose. يسهل 3D for .NET هذه العملية ، مما يضمن إدارة جميع التركيبات وتخزينها بشكل صحيح مع المشهد الذي تم تصديره. يوضح هذا الدليل كيفية تحقيق ذلك.

{{% /alert %}}

لتصدير مشهد وضمان حفظ جميع التركيبات المرتبطة في الدليل نفسه ، اتبع الخطوات التالية:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


جميع الكائنات `SaveOptions` في Aspose.3D تشمل خاصية `ExportTextures` ، والتي تبسط عملية إدارة القوام أثناء التصدير. تضمن هذه الخاصية حفظ جميع التركيبات ، سواء كانت خارجية أو مضمنة ، في دليل الإخراج المحدد. تتوافق هذه الميزة مع تنسيقات الملفات المتعددة التي تدعم تصدير النسيج ، مثل FBX و 3DS و OBJ و USD و GLTF و DAE.



شرح

1. تحميل المشهد: يتم تحميل المشهد من ملف الإدخال.
1. تهيئة خيارات التوفير: عيّن `ExportTextures` إلى `true`.
1. تصدير المشهد: يتم حفظ المشهد في دليل الإخراج مع مسارات النسيج المحدثة.


By leveraging the `ExportTextures` property in `SaveOptions`, you can seamlessly export 3D scenes along with their textures, ensuring that all necessary assets are organized in a single directory. This feature enhances the portability and ease of use of 3D files across various platforms and applications.

##  **Resources**

1. [البرنامج التعليمي عبر الإنترنت](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
