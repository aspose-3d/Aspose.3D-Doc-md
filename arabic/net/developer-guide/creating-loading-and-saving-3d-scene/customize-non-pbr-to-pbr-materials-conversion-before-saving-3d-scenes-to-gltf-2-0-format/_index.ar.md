---
title: تخصيص تحويل مواد بخلاف PBR إلى PBR قبل توفير 3D مشاهد إلى تنسيق GLTF 2.0 في C#
linktitle: تخصيص تحويل مواد غير PBR إلى PBR قبل توفير 3D مشاهد إلى تنسيق GLTF 2.0
type: docs
weight: 70
url: /ar/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose.3D API يحول داخليًا المواد غير المستخدمة في PBR إلى مواد PBR قبل التصدير إلى GLTF 2.0.
---
{{% alert color="primary" %}} 

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose. يحول 3D API داخليًا المواد غير PBR إلى مواد PBR قبل التصدير إلى GLTF 2.0 (ستظل المواد في المشهد دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
##  **Non-PBR إلى PBateraterateron**
يوضح مثال الشفرة C# هذا كيفية تحويل المادة إلى مادة PBR ، ثم يوفر مشهد 3D بتنسيق GLTF مع معالجة الملف C# 3D وتحويله API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **Resources**

1. [البرنامج التعليمي عبر الإنترنت](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
