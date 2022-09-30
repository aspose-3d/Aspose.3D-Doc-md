---
title: Aspose.3D for Java 18.10-أكتوبر 2018
type: docs
weight: 30
url: /ar/java/aspose-3d-for-java-18-10-october-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 18.10](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.10/).

{{% /alert %}} 
## **Ements proو Cمعلقة**


|**Sأوماري**|**Category**|
|:- |:- |
|Support for .NET منصة خام C|New eature|
|Allow المستخدم لإيقاف الضغط عند توفير FBX الملفات الثنائية|New eature|
|Import mproof FBX أداء الاستيراد|Enhancement|
|Improof FBX أداء الكتابة البولي|Enhancement|
|ImportException أثناء فتح ملفات ضخمة FBX|Bug|
|Problem مع property nitScaleFخاصية الممثل|Bug|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**

Pالإيجار عرض قائمة أي تغييرات أجريت على الجمهور API مثل إضافة ، إعادة تسميتها ، إزالة أو استبعاد الأعضاء وكذلك أي تغيير متوافق غير متخلف المحرز إلى Aspose.3D for Java API. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

## **API التغييرات:**

**أعضاء Added إلى الفئة 'com.aspose.threed. FBavaveOption'':**

{{< highlight "java" >}}

     /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public boolean com.aspose.threed.FBXSaveOptions.getEnableCompression();

    /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public void com.aspose.threed.FBXSaveOptions.setEnableCompression(boolean val);

{{< /highlight >}}





**Sوافرة oode:**

{{< highlight "java" >}}

     Scene scene = new Scene("test.fbx");

    FBXSaveOptions opts = new FBXSaveOptions(FileFormat.FBX7500_BINARY);

    opts.setEnableCompression(false);

    scene.save("test.fbx", opts);

{{< /highlight >}}
