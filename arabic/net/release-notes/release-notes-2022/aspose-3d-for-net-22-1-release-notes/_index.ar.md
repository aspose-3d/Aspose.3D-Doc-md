---
title: Aspose.3D for .NET 22.1 tes elease ootes
type: docs
weight: 12
url: /ar/net/aspose-3d-for-net-22-1-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.1.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1017 |تم تصميم دعم netstanard2.0|Ask اسأل|
|THREEDNET-1016 |Failed لفتح ملفات usdz لتحويل إلى glb|إصلاح g ug|
|THREEDNET-1018 |Odd FBX قضية تسبب في Msh تختفي|إصلاح g ug|
|THREEDNET-1020 |Entities dd الكيانات البدائية ترميز الدعم في USD المصدر|ميزة ew ew|
|THREEDNET-1021 |Entities dd الكيانات البدائية فك دعم في USD المصدر|ميزة ew ew|
|THREEDNET-1023 |كان التعامل مع tring غير صحيح في USD المستورد/المصدر|إصلاح g ug|
|THREEDNET-1022 |USD لا يمكن فتح الملف مع customData|إصلاح g ug|
|THREEDNET-1040 |الكائنات Multiple مع معرف الكائن المعين يدويا قد يسبب التصدير إلى FBX فشلت|إصلاح g ug|


## API التغييرات ##


In و 22.1 لقد قمنا بإصلاح بعض الأخطاء في FBX و USD ، وأضاف تصدير/تصدير بدائية إلى USD.

USD فقط دعم عدد قليل من البدائية مثل `Sphere` ، `Cube` ، `Cylinder` ، ونحن تصدير البدائية الأخرى من خلال USD customData ، ثم USD مشاهد تحويلها من الملفات CAD مثل RVM يمكن أن يكون حجم الملف أصغر بكثير.

And في 22.1 يمكن لبائع الويب دعم ملف USDZ مباشرة دون التحويل إلى تنسيق A3DW الآن.


### Added الفئة `Aspose.ThreeD.Formats.UsdSaveOptions`

`UsdSaveOptions` تسمح لك لتحديد كيفية التعامل مع البدائية أثناء التصدير ، وتحويلها إلى شبكة للحصول على أفضل التوافق أو حفظها كما هندسية البارامترات لأصغر حجم الملف ، لدينا بائع الويب يدعم هندسية البارامترات تصديرها من قبل Aspose.3D USDZ المصدر ، إنه الخيار الأفضل لك لتقديم محتوى 3D باستخدام مشغل الويب لدينا.



{{< highlight "csharp" >}}

        var scene = new Scene();
        scene.RootNode.CreateChildNode(new Cylinder());
        var opt = new UsdSaveOptions(FileFormat.USDZ);
        //default value is true for back compatibility, set it to false so we can generate smaller usdz file.
        opt.PrimitiveToMesh = false;
        scene.Save("test.usdz", opt);

{{< /highlight >}}
