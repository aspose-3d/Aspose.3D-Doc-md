---
title: تخصيص تحويل مواد غير PBR إلى PBR قبل توفير 3D مشاهد إلى تنسيق GLTF 2.0
type: docs
weight: 70
url: /ar/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose.3D API يحول داخليًا المواد غير المستخدمة في PBR إلى مواد PBR قبل التصدير إلى GLTF 2.0.
---
{{% alert color="primary" %}} 

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose. يحول 3D API داخليًا المواد غير PBR إلى مواد PBR قبل التصدير إلى GLTF 2.0 (ستظل المواد في المشهد دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
##  **Non-PBR إلى PBateraterateron**
This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

**C#**

```py

import aspose.threed as a3d

# initialize a new 3D scene

s = a3d.Scene()

box = a3d.Box()

mat = a3d.shading.PhongMaterial()
mat.diffuse_color = Vector3(1, 0, 1)

s.root_node.create_child_node("box1", box).material = mat

opt = a3d.formats.GLTFSaveOptions(FileFormat.GLTF2);

# save in GLTF 2.0 format

s.save("test.gltf", opt);

```
