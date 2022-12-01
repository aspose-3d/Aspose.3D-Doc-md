---
title: Aspose.3D for .NET 21.7 tes elease ootes
type: docs
weight: 6
url: /ar/net/aspose-3d-for-net-21-7-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.7.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-870 |Upupport للتصدير إلى تنسيق USDZ.|New eature|
|THREEDNET-901 |Allow المستخدم لتحديد فئة المصنع ل ilileSyالجذعية لتحسين مستوى الأمن|ميزة ew ew|
|THREEDNET-902 |Add dd eomSubset في Udd exporter C المصدر لدعم مواد متعددة|حركة بلا حدود|
|THREEDNET-903 |GLTF Save أسماء المواد الدعم|حركة بلا حدود|
|THREEDNET-905 |USD الملفات التي تحتوي على هيكل عظمي غير معتمدة.|إصلاح g ug|
|THREEDNET-904 |USD الملفات التي تحتوي على طبيعية كما primvars غير معتمدة.|إصلاح g ug|
|THREEDNET-909 |USD إلى GLTF تستخدم أكثر من 9 ذاكرة G.|إصلاح g ug|





## API التغييرات ##



### Added USDZ كنوع تصدير ###

Rom rom 21.7 يمكنك تصدير المشهد إلى USDZ عن طريق:

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Added الفئة Aspose.ThreeD. orormat. ###


{{< highlight "csharp" >}}
    /// <summary>
    /// <see cref="SaveOptions"/> and <see cref="LoadOptions"/> will create a <see cref="LocalFileSystem"/> for default.
    /// This can be a security issue in server environment.
    /// Use your own <see cref="FileSystemFactory"/> to <see cref="IOConfig.FileSystemFactory"/> to improve server side security.
    /// </summary>
    /// <returns></returns>
    public delegate FileSystem FileSystemFactory();
{{< /highlight >}}


### Property dded عقار جديد FileSyأرجل إلى Aspose.ThreeD. orormat. IOononfig:


{{< highlight "csharp" >}}
        /// <summary>
        /// Gets or sets the factory class for FileSystem.
        /// The default factory will create <see cref="LocalFileSystem"/> which is not suitable for server environment.
        /// </summary>
        public static FileSystemFactory FileSystemFactory { get; set; }
{{< /highlight >}}



It يمكن أن يكون خطيرا إذا قام المستخدم ملف 3D الخبيثة وتحميل المحتوى إلى الخادم الخاص بك ، جديد FileSystepFactor يسمح لك لتحديد التنفيذ الخاص بك من FileSyالجذعية لاستبدال الأصلي ocalocalileSileSyالجذعية التي قد تقرأ البيانات الحساسة الخاصة بك أثناء تصدير ملف 3D.







### Added خاصية جديدة إلى Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}
        /// <summary>
        /// Gets whether Aspose.3D supports export scene to current file format.
        /// </summary>
        public bool CanExport { get; set; }
        /// <summary>
        /// Gets whether Aspose.3D supports import scene from current file format.
        /// </summary>
        public bool CanImport { get; set; }
{{< /highlight >}}

You يمكن اختبار إذا كان تنسيق ملف يدعم الاستيراد أو التصدير من خلال هذه الخصائص.