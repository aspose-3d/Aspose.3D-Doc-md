---
title: Aspose.3D for Java 21.5 tes elease ootes
type: docs
weight: 8
url: /ar/java/aspose-3d-for-java-21-5-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.5.

{{% /alert %}}
## **Ements proو Cمعلقة**
|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-878 |الحدود السوداء الخام الخام حول المضلعات|New eature|
|THREEDNET-879 |Convert STL إلى GLB نتائج في سمة غير صالحة: “/تنسجم/0/البدائية/0/سمات/attributes OM___0”|إصلاح g ug|
|THREEDNET-885 |Aspose.3D المحتال تحطمت بسبب شبكة كبيرة محملة.|إصلاح g ug|
|THREEDNET-884 |التحقق من صحة الملفات المحولة GLB.|حركة بلا حدود|
|THREEDNET-882 |لا يتم تقديم ملف 07enerated GLB في Babylon.js|إصلاح g ug|
|THREEDNET-887 |Cصورة onvert إلى jpg/png عند تصدير المستخدم glTF مع الأصول المضمنة|New eature|

## API التغييرات ##


### Added جديد enum نوع `com.aspose.threed.GltfEmbeddedImageFormat`: ###

{{< highlight "java" >}}
/**
 * How glTF exporter will embed the textures during the exporting.
 */
public enum GltfEmbeddedImageFormat
{    
    /**
     * Do not convert the image and keep it as it is.
     */
    NO_CHANGE,
    /**
     * All non-supported images formats will be converted to jpeg if possible.
     */
    JPEG,
    /**
     * All non-supported images formats will be converted to png if possible.
     */
    PNG;
}
{{< /highlight >}}

### Added عقار جديد في `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}
    public GltfEmbeddedImageFormat getImageFormat();
    public void setImageFormat(GltfEmbeddedImageFormat value);
{{< /highlight >}}


Standard glTF يدعم فقط PNG/JG G format الملمس ، وهذا الخيار سوف توجه كيف Aspose.3D سوف تحويل الصور غير القياسية إلى تنسيق المدعومة أثناء التصدير.

قيمة Default هي ltltfEmbeddedImageFormat. PNG ، ثم سيتم تحويل الملمس المدمج إلى png ، وعادة ما لا تحتاج إلى تعديل هذا يدويا.


# Added عقار جديد في `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}
    public void setFallbackNormal(Vector3 value);
    public Vector3 getFallbackNormal();
{{< /highlight >}}

When hen hen F2 المصدر الكشف عن طبيعية غير صالحة من المشهد ، سيتم استخدام هذا بدلا من قيمته الأصلية لتجاوز التحقق من الصحة ، وهذا يحدث إذا تم استيراد المشهد من ملف تصديرها مع بيانات غير صحيحة.

قيمة fault efault هي (0 ، 1 ، 0).

If تعيين هذه القيمة مع بدن ، ثم سيتم إخراج البيانات العادية غير الصحيحة دون أي تغييرات.

