---
title: إضافة معلومات الأصول إلى مستند 3D
type: docs
weight: 10
url: /ar/java/add-asset-information-to-3d-document/
description: البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for Java API لديه دعم لتحديد البيانات الوصفية للمشهد.
---
##  **إضافة معلومات الأصول إلى مستند 3D**
البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for Java API لديه دعم لتحديد البيانات الوصفية للمشهد.
###  **Define أ etetadata للمشهد**
3D shows produce massive quantities of metadata and picture information. Metadata is an asset and part of the show.

1. قم بتهيئة مشهد 3D باستخدام فئة `Scene`.
1. تطبيق Set/اسم الأداة.
1. Set تطبيق/أداة اسم البائع.
1. وحدة قياس et et.
1. مقياس وحدة القياس et et.
1. وفِّر 3D مشهد في تنسيق الملف المدعوم.

في هذا المثال ، نفترض أن المشهد تم إنشاؤه بواسطة أداة CAD تُسمى بمصر ، وقد صممها مكتب Manualdesk:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
