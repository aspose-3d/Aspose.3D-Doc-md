---
title: Customize Non-PBR إلى aterateraterالمواد ononedition قبل aving aving 3D cencenes إلى GLTF 2.0 orormat في C#
linktitle: Customize Non-PBR إلى aterateraterالمواد ononقبل aving aving 3D cencenإلى GLTF 2.0 orormat
type: docs
weight: 70
url: /ar/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: The Scene فئة من Aspose.3D API يمثل مشهد 3D. Dإيفلين يمكن بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. GLTF 2.0 يدعم فقط PBR (Physally ased ased en) المواد ، Aspose.3D API يحول داخليا المواد غير PBR إلى مواد PBقبل التصدير إلى GLTF 2.0.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) فئة من Aspose.3D API يمثل مشهد 3D. Dإيفلين يمكن بالفعل بناء مشهد 3D عن طريق إضافة كيانات مختلفة. GLTF 2.0 يدعم فقط PBR (Physally ased ased en) المواد ، Aspose.3D API يحول داخليا المواد غير Pased ased إلى مواد PR قبل التصدير إلى GLTF 2.0 (المواد في المشهد ستبقى دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
## **Non-PBR إلى PBateraterateron**
Tله C# رمز مثال يوضح كيفية تحويل المواد إلى المواد PBR ، ومن ثم يوفر 3D المشهد في تنسيق GLTF مع C# 3D ملف التلاعب والتحويل API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
