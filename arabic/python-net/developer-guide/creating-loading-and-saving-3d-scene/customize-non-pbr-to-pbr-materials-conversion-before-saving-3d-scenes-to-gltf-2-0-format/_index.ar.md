---
title: Customize Non-PBR إلى aterateraterالمواد ononقبل aving aving 3D cencenإلى GLTF 2.0 orormat
type: docs
weight: 70
url: /ar/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: The Scene فئة من Aspose.3D API يمثل مشهد 3D. Dإيفلين يمكن بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. GLTF 2.0 يدعم فقط PBR (Physally ased ased en) المواد ، Aspose.3D API يحول داخليا المواد غير PBR إلى مواد PBقبل التصدير إلى GLTF 2.0.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) فئة من Aspose.3D API يمثل مشهد 3D. Dإيفلين يمكن بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. GLTF 2.0 يدعم فقط PBR (Physally ased ased en) المواد ، Aspose.3D API يحول داخليا المواد غير Pased ased إلى مواد PR قبل التصدير إلى GLTF 2.0 (المواد في المشهد ستبقى دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
## **Non-PBR إلى PBateraterateron**
Tمثال التعليمات البرمجية له يوضح كيفية تحويل المواد إلى المواد PBR ، ومن ثم يحفظ 3D المشهد في تنسيق GLTF:

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
