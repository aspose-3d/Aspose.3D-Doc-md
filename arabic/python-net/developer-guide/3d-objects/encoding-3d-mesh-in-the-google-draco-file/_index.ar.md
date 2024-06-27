---
title: ترميز 3D شبكة في ملف Google Draco
type: docs
weight: 60
url: /ar/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: يسمح Aspose.3D for Python via .NET API للمطورين باستيراد نموذج 3D ، ثم ترميز الشبكات في ملفات Google Draco. يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.
---
{{% alert color="primary" %}}

يسمح [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API للمطورين بـ [استيراد طراز 3D](/3d/ar/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene) ، ثم ترميز الشبكات في ملفات Google Draco. يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.

{{% /alert %}}
##  **استرداد شبكة 3D وترميز في ملف Google Draco**
يمكن استخدام طريقة `encode` التي تعرضها فئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) لترميز شبكة ثلاثية الأبعاد في ملف Google Draco. يتطلب الأمر وجود كائنات [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) و [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) كمعلمات. باستخدام خيارات الحفظ Draco ، يمكن للمطورين أيضًا تحديد الموضع ، إحداثيات النسيج ، واللون والبتات العادية بالإضافة إلى مستوى الضغط قبل تشفير شبكة.
###  **Pروغرامينغ ple وافرة**
يسترد هذا المثال البرمجي شبكة كروية ، ثم يرمز في الملف Google Draco بعد تحديد مستوى الضغط.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
