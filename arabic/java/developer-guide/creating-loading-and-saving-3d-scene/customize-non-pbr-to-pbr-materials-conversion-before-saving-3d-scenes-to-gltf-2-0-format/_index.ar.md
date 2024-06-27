---
title: تخصيص تحويل مواد غير PBR إلى PBR قبل توفير 3D مشاهد إلى تنسيق GLTF 2.0
type: docs
weight: 50
url: /ar/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: فئة المشهد لـ Aspose.3D for Java API يمثل مشهد 3D ويمكن للمطورين إنشاء مشهد 3D بإضافة كيانات مختلفة.
---
{{% alert color="primary" %}} 

فئة `Scene` من Aspose.3D for Java API تمثل مشهد 3D ويمكن للمطورين إنشاء مشهد 3D بإضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose. يحول 3D API داخليًا المواد غير المعالجة بالكمبيوتر إلى مواد PBR قبل التصدير إلى GLTF 2.0 (ستظل المواد في المشهد دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
##  **Non-PBR إلى PBateraterateron**
This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
