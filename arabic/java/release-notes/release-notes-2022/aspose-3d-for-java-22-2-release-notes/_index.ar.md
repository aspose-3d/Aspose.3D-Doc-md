---
title: Aspose.3D for Java 22.2 tes elease ootes
type: docs
weight: 11
url: /ar/java/aspose-3d-for-java-22-2-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.2.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEJava-1054|Embed llow تضمين القوام في U3D و PDF ملف|ميزة ew ew|
|THREEJava-1058|لا يمكن ربط ريمياثيس إلى المواد في USD المصدر/المستورد|إصلاح g ug|
|THREEJava-1051|إضافات الوصول Allow والإضافات في ملف GLTF|حركة بلا حدود|
|THREEJava-1048|Allow ترميز المشهد والبيانات الفوقية عقدة إلى usd|ميزة ew ew|
|THREEJava-1049|Allow فك المشهد والبيانات الفوقية عقدة من usd|ميزة ew ew|

## API التغييرات ##


### أعضاء Added إلى الفئة com.aspose.threed. sssetInfo:

{{< highlight "java" >}}
    /**
     * Gets the document's copyright
     */
    public String getCopyright();

{{< /highlight >}}

Gets حقوق الطبع والنشر للملف ، يمكن أن تكون هذه القيمة لاغية أو محددة في ملف 3D.
Only USC C/USDZ دعم هذه المنشأة الآن.

NOTE: hangمعلقة في هذه الخاصية لن تغير قسم حقوق الطبع والنشر من ملف الإخراج 3D.


### أعضاء Added إلى الفئة `com.aspose.threed.UsdSaveOptions`:

{{< highlight "csharp" >}}
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     */
    public boolean getExportMetaData();
    
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     * @param value New value
     */
    public void setExportMetaData(boolean value);

{{< /highlight >}}

Gets أو يحدد ما إذا كان تصدير معلومات الأصول المشهد وخصائص عقدة إلى الإخراج USDC/USDZ الملف.



### أعضاء Added إلى الفئة `com.aspose.threed.PdfSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the PDF file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the PDF file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}

Set هذا إلى true لتوليد ملف 3D PDF مع ملفات الملمس المضمنة.

Eرمز xample:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.pdf", opt);
{{< /highlight >}}


### أعضاء Added إلى الفئة `com.aspose.threed.U3dSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the U3D file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the U3D file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);

{{< /highlight >}}

Set هذا إلى true لتوليد ملف 3D U3D مع ملفات الملمس المضمنة.

Eرمز xample:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.u3d", opt);
{{< /highlight >}}



