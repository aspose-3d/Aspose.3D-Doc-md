---
title: Aspose.3D for .NET 21.6 tes elease ootes
type: docs
weight: 7
url: /ar/net/aspose-3d-for-net-21-6-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.6.

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
    scene.Save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Added فئة جديدة Aspose.ThreeD. ###

يمكن لـ glt لـ glb/fbx وغيرها من تنسيقات الملفات التي تدعم تضمين الملمس للوصول إلى الأصول الخارجية من خلال ملف zip باستخدام ipipArchiveFileSyالجذعية إلى ptions aveOptions.


### Added خاصية جديدة إلى الفئة Aspose.ThreeD. orormat. ptions bxSaveOptions ###

{{< highlight "csharp" >}}
    /// <summary>
    /// Gets or sets whether to embed the texture to the final output file.
    /// FBX Exporter will try to find the texture's raw data from <see cref="IOConfig.FileSystem"/>, and embed the file to final FBX file.
    /// Default value is false.
    /// </summary>
    public bool EmbedTextures{ get;set;}
{{< /highlight >}}


Sرمز وافرة:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.EmbedTextures = true;
    var tex = new Texture();
    tex.FileName = "test.png";
    tex.SetProperty("RelativeFilename", "test.png");
    var mat = new PhongMaterial();
    mat.SetTexture(Material.MapDiffuse, tex);
    var planeNode = scene.RootNode.CreateChildNode(new Plane());
    planeNode.Material = mat;
    scene.Save("plane-with-texture.fbx", opt);

{{< /highlight >}}


### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions 3Dptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ptions
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. Discreet3Dptions
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. Discreet3Dptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions Tptions ptions 5 ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions ptions ptions ptions ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.

### Rالرموز التعبيرية فئة obsoleted Aspose.ThreeD. orormat. ptions 3Dptions oadOالوصفات ###
تم وضع علامة على صفه كما obsoleted قبل أشهر.
