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

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **نظام تنسيق قابل للطي بتنسيقات 3D**
Aspose.3D for Python via .NET API يسمح للمستخدمين بقلب نظام الإحداثيات بتنسيقات OBJ و 3DS و STL و U3D.

{{% alert color="primary" %}} 

لاستيراد ملف 3ds وحفظه بتنسيق OBJ يتم استخدام فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) في الرمز.

{{% /alert %}} 

في هذا المثال ، قلبنا نظام الإحداثيات أثناء استيراد ملف 3ds ، وحفظناه بتنسيق OBJ بدون مواد.
