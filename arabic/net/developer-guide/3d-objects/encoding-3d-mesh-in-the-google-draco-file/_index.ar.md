---
title: ترميز 3D شبكة في ملف Google Draco
type: docs
weight: 60
url: /ar/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API يسمح للمطورين باستيراد طراز 3D ، ثم ترميز الشبكات في ملفات Google Draco. يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.
---
{{% alert color="primary" %}}

يسمح [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API للمطورين بـ [استيراد طراز 3D](/3d/ar/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene) ، ثم ترميز الشبكات في ملفات Google Draco. يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.

{{% /alert %}}
##  **استرداد شبكة 3D وترميز في ملف Google Draco**
يمكن استخدام طريقة `Encode` التي تعرضها فئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) لترميز شبكة ثلاثية الأبعاد في ملف Google Draco. يتطلب الأمر وجود كائنات [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) و [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) كمعلمات. باستخدام خيارات الحفظ Draco ، يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.
###  **Pروغرامينغ ple وافرة**
This code example retrieves a `Mesh` of `Sphere`, and then encode in the Google Draco file after specifying a compression level.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
