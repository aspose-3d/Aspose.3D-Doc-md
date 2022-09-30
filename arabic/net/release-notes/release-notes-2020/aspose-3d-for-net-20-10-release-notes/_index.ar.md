---
title: Aspose.3D for .NET 20.10 tes elease ootes
type: docs
weight: 7
url: /ar/net/aspose-3d-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 20.10.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-737 |Add الدعم البدائي في A3DW التصدير/الاستيراد.|
|THREEDNET-732 |Aspose.3D لديه خطأ الملمس عند توليد GLTF ، ولكن لا توجد مشكلة حفظه كما FBX|
|THREEDNET-738 |Add دعم جدول الألوان في ملف RVM.|
|THREEDNET-739 |Upupport ل 7.7/inary البولي/Autooffice FBX|

## API التغييرات ##

### Formats dded تنسيقات الملفات الجديدة إلى الفئة Aspose.ThreeD.FileFormat:

{{< highlight "java" >}}

    public static readonly Aspose.ThreeD.FileFormat FBX7600ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7600Binary;
    public static readonly Aspose.ThreeD.FileFormat FBX7700ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7700Binary;

{{< /highlight >}}

Now يمكنك تصدير المشهد إلى FBX 7.6/7.7 في ASCII/وضع البولي B.

Sرمز وافرة:

{{< highlight "java" >}}

    Scene scene = new Scene(new Pyramid());
    scene.Save("fbx7.7.fbx", FileFormat.FBX7700ASCII);

{{< /highlight >}}


### Added فئة جديدة Aspose.ThreeD. orormat. A3Dptions ptions aveOptions

{{< highlight "java" >}}

    /// <summary>
    /// Save options for A3DW format.
    /// </summary>
    public class A3DWSaveOptions : SaveOptions
    {
        /// <summary>
        /// Export meta data associated with Scene/Node to client
        /// Default value is true
        /// </summary>
        public bool ExportMetaData { get; set; }

        /// <summary>
        /// If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
        /// </summary>
        public string MetaDataPrefix { get; set; }
    }

{{< /highlight >}}

Tانه جديد A3Dptions ptions aveOptions يسمح لك لتصدير معلومات الأصول والخصائص إلى ملف A3DW.

يتم استخدام Tمع بائع الويب الجديد.

{{< highlight "java" >}}

    Scene scene = new Scene();
    scene.RootNode.CreateChildNode(new Pyramid()).SetProperty("rvm:No", "347923");
    scene.Save("test.a3dw", new A3DWSaveOptions() { MetaDataPrefix = "rvm:" });

{{< /highlight >}}
