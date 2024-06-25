---
title: إضافة معلومات أصول ونظام إحداثيات الوجه بتنسيقات 3D
type: docs
weight: 10
url: /ar/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for Python via .NET API يسمح للمطورين بتحديد بيانات وصفية للمشهد.
---
##  **إضافة معلومات أصل إلى مشهد 3D**
البيانات الوصفية عبارة عن معلومات منظمة تصف أو توضح أو تحدد أو تجعل استرداد أو استخدام أو إدارة مورد معلومات أسهل. Aspose.3D for Python via .NET API يسمح للمطورين بتحديد بيانات وصفية للمشهد.
###  **Define أ etetadata للمشهد**
3D shows produce massive quantities of metadata and picture information. Metadata is an asset and part of the show.

1. قم بتهيئة مشهد 3D باستخدام فئة `Scene`.
1. تطبيق Set/اسم الأداة.
1. Set تطبيق/أداة اسم البائع.
1. وحدة قياس et et.
1. مقياس وحدة القياس et et.
1. وفِّر 3D مشهد في تنسيق الملف المدعوم.

في هذا المثال ، نفترض أن المشهد تم إنشاؤه بواسطة أداة CAD تُسمى بمصر ، وقد صممها مكتب Manualdesk:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **نظام تنسيق قابل للطي بتنسيقات 3D**
Aspose.3D for Python via .NET API يسمح للمستخدمين بقلب نظام الإحداثيات بتنسيقات OBJ و 3DS و STL و U3D.

{{% alert color="primary" %}} 

لاستيراد ملف 3ds وحفظه بتنسيق OBJ يتم استخدام فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) في الرمز.

{{% /alert %}} 

في هذا المثال ، قلبنا نظام الإحداثيات أثناء استيراد ملف 3ds ، وحفظناه بتنسيق OBJ بدون مواد.
