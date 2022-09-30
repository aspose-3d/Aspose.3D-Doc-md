---
title: Aspose.3D for .NET 21.4 tes elease ootes
type: docs
weight: 9
url: /ar/net/aspose-3d-for-net-21-4-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.4.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-864 |Property mplement property ileStream الملكية ل exexture lass لاس لتحميل الصورة من تيار|حركة بلا حدود|
|THREEDNET-867 |Large ملف obj يستغرق الكثير من الوقت لتحميل|حركة بلا حدود|
|THREEDNET-865 |Add dd utooffice Navisworks مواد متوافقة لتنسيق RVM|حركة بلا حدود|
|THREEDNET-874 |Add دعم أحدث تنسيق RVM.|حركة بلا حدود|
|THREEDAPP-94 |Iأثبت أداء تحميل بائع الويب|حركة بلا حدود|
|THREEDNET-851 |Allow استخدام التنفيذ الخارجي من Draco التشفير.|حركة بلا حدود|
|THREEDNET-876 |Encoder mproof بنيت tin Draco التشفير/فك الأداء.|حركة بلا حدود|
|THREEDNET-862 |لا يمكن فتح ملف glb onverted بواسطة أدوات الطرف 3rd.|إصلاح g ug|
|THREEDNET-863 |فشل onمن USDZ إلى STL|إصلاح g ug|
|THREEDNET-866 |FBX إلى gltf/glb ExportException: لا يتم دعم نوع Oحقن Aspose.ThreeD.|إصلاح g ug|
|THREEDNET-873 |Collada تصديرها من قبل Frosty Suite لا يمكن استيرادها.|إصلاح g ug|
|THREEDNET-872 |Collada تصديرها من قبل خلاط/ليغو أداة لا يمكن استيرادها.|إصلاح g ug|
|THREEDNET-871 |لا يمكن فتح ملفات ome ome ipipped 3D من قبل Aspose.3D|إصلاح g ug|
|THREEDNET-869 |لا يتم التعرف على ملفات ome ome STL|إصلاح g ug|
|THREEDAPP-114 |لا يمكن فتح ملفات inary STL بدون رأس ثنائي صريح.|إصلاح g ug|


## API التغييرات ##


Tنسخته هي أساسا إصدار إصلاح الأخطاء ، الثابتة مجموعة من الأخطاء ، وتحسين مجموعة من مشاكل التوافق والعروض ل FBX ، Collada ، STL ، obj ، drc ، gltf ، glb.



ملاحظة عدد قليل من التغييرات الطفيفة API.

### Added خاصية جديدة في الفئة Aspose.ThreeD. orormat. ptions ltfSaveOالوصفات:

{{< highlight "csharp" >}}

    /// <summary>
    /// Use external draco encoder to accelerate the draco compression speed.
    /// </summary>
    /// <remarks>
    /// Aspose.3D will create new sub process to encode the mesh to the draco format, use it at your own risk. 
    /// </remarks>
    public string ExternalDracoEncoder { get; set; }

{{< /highlight >}}


Aspose.3D ل. صافي 21.4 لديه ضعف تحسين الأداء ل Draco من الإصدارات القديمة ، ولكن التنفيذ الرسمي Google الذي كتب في C++ لا يزال أسرع ، لذلك نحن تمكين المستخدم لاستخدام الخارجية Draco التشفير لأداء أفضل.

Sرمز وافرة لاستخدام التشفير الرسمي الخارجي لتسريع مضغوط GLB الجيل:

{{< highlight "csharp" >}}

    var mesh = new Sphere();
    var scene = new Scene(mesh);
    var opt = new GltfSaveOptions(FileFormat.GLTF2_Binary);
    opt.ExternalDracoEncoder = @"D:\Github\draco\sln\Release\draco_encoder.exe";
    opt.DracoCompression = true;
    scene.Save("test.glb", opt);

{{< /highlight >}}

{{% alert color="primary" %}} 
NOTE: سيتم وضع علامة على هذه الخاصية بأنها obsoleted بمجرد تحسين أداء ترميز/فك تشفير draco إلى مستوى التنفيذ الرسمي.
{{% /alert %}}