---
title: إضافة معلومات الأصول إلى المشهد
type: docs
weight: 10
url: /ar/net/add-an-asset-information-to-scene
description: البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for .NET API يسمح للمطورين بتحديد بيانات وصفية للمشهد.
---
##  **إضافة معلومات أصل إلى مشهد 3D**
البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for .NET API يسمح للمطورين بتحديد بيانات وصفية للمشهد.
###  **Define أ etetadata للمشهد**
3D shows produce massive quantities of metadata and picture information. Metadata is an asset and part of the show.

1. قم بتهيئة مشهد 3D باستخدام فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene).
1. تطبيق Set/اسم الأداة.
1. Set تطبيق/أداة اسم البائع.
1. وحدة قياس et et.
1. مقياس وحدة القياس et et.
1. وفِّر 3D مشهد في تنسيق الملف المدعوم.

في هذا المثال ، نفترض أن المشهد تم إنشاؤه بواسطة أداة CAD تُسمى بمصر ، وقد صممها مكتب Manualdesk:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
