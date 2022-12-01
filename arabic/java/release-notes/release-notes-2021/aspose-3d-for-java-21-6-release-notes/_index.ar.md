---
title: Aspose.3D for Java 21.6 tes elease ootes
type: docs
weight: 7
url: /ar/java/aspose-3d-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.6.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-870 |Add dd SDC دعم التصدير.|New eature|
|THREEDNET-891 |نظام ملف الأرشيف البريدي x|New eature|
|THREEDNET-892 |Allow FBX المصدر لتضمين القوام أثناء التصدير.|ميزة ew ew|
|THREEDNET-895 |Ixixed بعض الأحرف في اسم العقدة سوف يسبب ملف تم إنشاؤه GLB فشل في تمرير التحقق من الصحة|إصلاح g ug|
|THREEDNET-896 |Fixed المشهد فارغة لا يمكن تصديرها إلى ملف glb صالح|إصلاح g ug|
|THREEDNET-890 |Add المواد/تصدير الملمس في Udd dd C|حركة بلا حدود|
|THREEDNET-899 |Expose خاصية RelativeFilename ل FBX exexture|حركة بلا حدود|




## API التغييرات ##


### Added USD كنوع تصدير ###

Rom rom 21.6 يمكنك تصدير المشهد إلى ملف USD عن طريق:

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Added فئة جديدة com.aspose.threed. ipipArchiveFileSyالجذعية ###

يمكن لـ glt لـ glb/fbx وغيرها من تنسيقات الملفات التي تدعم تضمين الملمس للوصول إلى الأصول الخارجية من خلال ملف zip باستخدام ipipArchiveFileSyالجذعية إلى ptions aveOptions.


### Added عقار جديد إلى الفئة com.aspose.threed. bxbxSaveOptions ###

{{< highlight "csharp" >}}
    /**
     * Gets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Sets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}


Sرمز وافرة:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.setEmbedTextures(true);
    var tex = new Texture();
    tex.setFileName("test.png");
    var mat = new PhongMaterial();
    mat.setTexture(Material.MAP_DIFFUSE, tex);
    var planeNode = scene.getRootNode().createChildNode(new Plane());
    planeNode.setMaterial(mat);
    scene.save("plane-with-texture.fbx", opt);
{{< /highlight >}}

