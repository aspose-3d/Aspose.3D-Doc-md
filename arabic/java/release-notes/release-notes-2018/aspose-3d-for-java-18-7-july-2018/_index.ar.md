---
title: Aspose.3D for Java 18.7 - July 2018
type: docs
weight: 60
url: /ar/java/aspose-3d-for-java-18-7-july-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 18.7](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.7/).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Sأوماري**|**Category**|
|:- |:- |
|Add Draco 2.2 دعم الاستيراد|New eature|
|Add Draco 2.2 دعم التصدير|New eature|
|Import glTF الملفات مع ضغط دراكو|New eature|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
Pالإيجار عرض قائمة أي تغييرات أجريت على الجمهور API مثل إضافة ، إعادة تسميتها ، إزالة أو استبعاد الأعضاء وكذلك أي تغيير متوافق غير متخلف المحرز إلى Aspose.3D for Java API. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

## **API التغييرات:**

**3 أعضاء إزالتها من الفئة com.aspose.threed. roroperty:**

{{< highlight "java" >}}

     public void com.aspose.threed.Property.setExtraData(java.lang.String);

    public java.lang.String com.aspose.threed.Property.getExtraData();

    public int com.aspose.threed.Property.getFlags();

{{< /highlight >}}

تتم إزالة These لمزامنة التغييرات من .NET الإصدار. (Tمن المقرر إزالتها منذ Aspose.3D for .NET 18.2)

**1 خاصية تضاف إلى الفئة com.aspose.threed. bjbjLoadOptions:**

{{< highlight "java" >}}

     public boolean com.aspose.threed.ObjLoadOptions.getNormalizeNormal();

    public void com.aspose.threed.ObjLoadOptions.setNormalizeNormal(boolean);

{{< /highlight >}}

Ets ets أو يحدد ما إذا كان لتطبيع ناقلات العادية أثناء التحميل ، القيمة الافتراضية صحيحة.

**Sرمز وافرة:**

{{< highlight "java" >}}

         Scene scene = new Scene();

        ObjLoadOptions opt = new ObjLoadOptions();

        opt.setNormalizeNormal(false);

        scene.open("test.obj", opt);

{{< /highlight >}}

Tله سوف تحميل ملف obj وترك ناقلات العادية غير طبيعية ، فإن النسخة القديمة تطبيع ناقلات العادية عند تحميل ملف obj.
