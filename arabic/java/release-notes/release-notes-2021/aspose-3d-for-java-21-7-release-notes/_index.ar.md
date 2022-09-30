---
title: Aspose.3D for Java 21.7 tes elease ootes
type: docs
weight: 6
url: /ar/java/aspose-3d-for-java-21-7-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.7.

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

{{< highlight "java" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Added فئة com.aspose.threed. ###


{{< highlight "java" >}}
    /**
    * {@link com.aspose.threed.SaveOptions} and {@link com.aspose.threed.LoadOptions} will create a {@link com.aspose.threed.LocalFileSystem} for default.
    * This can be a security issue in server environment.
    * Use your own {@link com.aspose.threed.FileSystemFactory} to {@link com.aspose.threed.IOConfig#getFileSystemFactory} to improve server side security.
    */
    public interface FileSystemFactory
    {    
        FileSystem call();
        
    }
{{< /highlight >}}


### Property dded الملكية الجديدة FileSyالاحدث إلى com.aspose.threed. Iononfig:


{{< highlight "java" >}}
    /**
     * Gets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     */
    public static FileSystemFactory getFileSystemFactory();
    
    /**
     * Sets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     * @param value New value
     */
    public static void setFileSystemFactory(FileSystemFactory value);

{{< /highlight >}}



It يمكن أن يكون خطيرا إذا قام المستخدم ملف 3D الخبيثة وتحميل المحتوى إلى الخادم الخاص بك ، جديد FileSystepFactor يسمح لك لتحديد التنفيذ الخاص بك من FileSyالجذعية لاستبدال الأصلي ocalocalileSileSyالجذعية التي قد تقرأ البيانات الحساسة الخاصة بك أثناء تصدير ملف 3D.







### Added خاصية جديدة إلى com.aspose.threed. ilileFormat:

{{< highlight "java" >}}
    /**
     * Gets whether Aspose.3D supports export scene to current file format.
     */
    public boolean getCanExport();
    
    /**
     * Gets whether Aspose.3D supports import scene from current file format.
     */
    public boolean getCanImport();

{{< /highlight >}}

You يمكن اختبار إذا كان تنسيق ملف يدعم الاستيراد أو التصدير من خلال هذه الخصائص.