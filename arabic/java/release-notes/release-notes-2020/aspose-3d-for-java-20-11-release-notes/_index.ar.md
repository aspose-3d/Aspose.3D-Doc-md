---
title: Aspose.3D for Java 20.11 tes elease ootes
type: docs
weight: 6
url: /ar/java/aspose-3d-for-java-20-11-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 20.11.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-747 |Rأندر خطوط الحافة لأنواع CAD في بائع الويب.|إصلاح g ug|
|THREEDNET-748 |Improof الإضاءة في بائع الويب|إصلاح g ug|
|THREEDNET-755 |Attributes nsupport سمات نموذج في بعض الملفات FBX 6.1.|إصلاح g ug|
|THREEDNET-757 |PLY لا يتم دعم الملف مع خاصية int64.|إصلاح g ug|
|THREEDNET-756 |3MF لا يمكن فتح الملف المصدرة باستخدام أحدث المعايير.|إصلاح g ug|
|THREEDNET-758 |FBX 6.0 لا يمكن استيراد الملف.|إصلاح g ug|
|THREEDNET-760 |Improof توافق الملفات ASE|إصلاح g ug|
|THREEDNET-761 |Allow تحديد الترميز لملفات 3D المستندة إلى النص.|حركة بلا حدود|
|THREEDNET-762 |Eمشهد xport إلى HTML باستخدام أحدث بائع لدينا.|ميزة ew ew|
|THREEDNET-763 |دعم dd dd من كولدا غير القياسية تصديرها من قبل مصدر غير معروف.|حركة بلا حدود|
|THREEDNET-765 |Optimize أداء التحميل من الملف الثنائي PLY|Improof|
|THREEDNET-768 |لا يمكن استيراد الملف البولي STL المصدرة من قبل hinhinoceros.|إصلاح g ug|
|THREEDNET-769 |دعم العلاقات في FBX 6.0|إصلاح g ug|
|TRHEEDNET-770 |سوف يؤدي حرف الهروب غير الصحيح في ملف FBX إلى فشل Aspose.3D في الاستيراد.|إصلاح g ug|
|THREEDNET-771 |Add تضمين دعم البيانات في FBX|إصلاح g ug|


## API التغييرات ##


Tانه التغيير الرئيسي في هذا الإصدار هو تصدير ملف HTML5 لن تستخدم المستأجر القديم.

يتم استخدام rennوز renebAالقائم على الجمعية لتقديم.

تم إصلاح الكثير من الأخطاء في هذا الإصدار.

### Added خاصية جديدة إلى الفئة com.aspose.threed. erertexEleالقابل UserData:

{{< highlight "java" >}}

    /**
     * Gets the indices data
     */
    @Override
    public List<Integer> getIndices();

{{< /highlight >}}

Tيتم إضافة ممتلكاته لذلك تحتوي ملفات fbx على بيانات المستخدم التي تشير إليها يمكن استيرادها بشكل صحيح.


### Added عقار جديد إلى الفئة com.aspose.threed. Ionononfig:

{{< highlight "java" >}}

    /**
     * Gets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     */
    public Charset getEncoding();
    
    /**
     * Sets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     * @param value New value
     */
    public void setEncoding(Charset value);

{{< /highlight >}}

Tيستخدم لتجاوز الترميز الداخلي الافتراضي أثناء الاستيراد/التصدير ، حتى تتمكن من التحكم يدويا في ترميز الأشكال المستندة إلى النص.