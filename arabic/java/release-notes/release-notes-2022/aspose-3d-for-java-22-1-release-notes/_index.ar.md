---
title: Aspose.3D for Java 22.1 tes elease ootes
type: docs
weight: 12
url: /ar/java/aspose-3d-for-java-22-1-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.1.

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

USD فقط دعم عدد قليل من البدائية مثل ere phere ، Cube ، Cylinder ، ونحن تصدير البدائية الأخرى من خلال USD customData ، ثم USD مشاهد تحويلها من الملفات CAD مثل RVM يمكن أن يكون حجم ملف أصغر بكثير.

And في 22.1 يمكن لبائع الويب دعم ملف USDZ مباشرة دون التحويل إلى تنسيق A3DW الآن.


### Added فئة Aspose.ThreeD. orormat. ptions sdSaveOptions

تسمح لك اختبارات sdsdSaveOبتحديد كيفية التعامل مع البدائية أثناء التصدير ، وتحويلها إلى شبكة للحصول على أفضل توافق أو حفظها كنماذج هندسية متناظرة لأصغر حجم ملف ، يدعم جهاز عرض الويب لدينا الهندسة البارامترية المصدرة من قبل Aspose.3D USDZ المصدر ، إنه الخيار الأفضل لك لتقديم محتوى 3D باستخدام مشغل الويب لدينا.



{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Cylinder());
    var opt = new UsdSaveOptions(FileFormat.USDZ);
    //default value is true for back compatibility, set it to false so we can generate smaller usdz file.
    opt.setPrimitiveToMesh(false);
    scene.save("test.usdz", opt);

{{< /highlight >}}
