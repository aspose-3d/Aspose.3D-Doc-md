---
title: Aspose.3D for Java 22.9 tes elease ootes
type: docs
weight: 4
url: /ar/java/aspose-3d-for-java-22-9-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for Java 22.9.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.9.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1232 |Add دعم نظام الملفات المؤقتة الداخلية للمستورد FBX|حركة بلا حدود|
|THREEDNET-1111 |GLTF التصدير غير جيد|تحديد g ug|
|THREEDNET-1215 |When استيراد ملف OBJ ، عقدة واحدة يمكن قراءة مادة واحدة فقط ؟|تحديد g ug|
|THREEDNET-1216 |Converting GLB إلى GLB يفقد القوام|تحديد g ug|
|THREEDNET-1225 |قضايا Anallze وجدت في خادم pp A- 2022 في أيلول/سبتمبر|تحديد g ug|
|THREEDNET-1227 |خيارات غير مدعومة في ASE الملفات: MAT070707AL_SOFTEN/PHYSQUE/MATERAL L_SHIE E|تحديد g ug|
|THREEDNET-1228 |Xcxception عند استيراد ملفات JT: تم إضافة عنصر An بنفس المفتاح بالفعل|تحديد g ug|
|THREEDNET-1230 |STL الملفات ذات الوجه الرباعي غير معتمدة.|تحديد g ug|
|THREEDNET-1231 |Unsupport USD نوع StringVector ، LayerOffsetVector|تحديد g ug|


## API التغييرات ##


### Added طريقة جديدة في الفئة `com.aspose.threed.PbrMaterial`:

{{< highlight "java" >}}
    /**
     * Allow convert other material to PbrMaterial
     * @param material 
     */
    public static PbrMaterial fromMaterial(Material material)

{{< /highlight >}}


Tطريقة فائدة له يسمح تحويل أنواع أخرى من المواد إلى `PbrMaterial` سبيل المثال ، ومحاولة حجز المعلومات قدر الإمكان.


