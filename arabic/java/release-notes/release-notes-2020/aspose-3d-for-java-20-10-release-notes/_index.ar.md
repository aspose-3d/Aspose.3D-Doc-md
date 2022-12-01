---
title: Aspose.3D for Java 20.10 tes elease ootes
type: docs
weight: 7
url: /ar/java/aspose-3d-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 20.10.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-737 |Add الدعم البدائي في A3DW التصدير/الاستيراد.|
|THREEDNET-732 |Aspose.3D لديه خطأ الملمس عند توليد GLTF ، ولكن لا توجد مشكلة حفظه كما FBX|
|THREEDNET-738 |Add دعم جدول الألوان في ملف RVM.|
|THREEDNET-739 |Upupport ل 7.7/inary البولي/Autooffice FBX|


## API التغييرات ##

### Added تنسيقات الملفات الجديدة إلى الفئة com.aspose.threed. ilileFormat:

{{< highlight "java" >}}
    /**
     * ASCII FBX file format, with 7.6.0 version
     */
    public static final FileFormat FBX7600ASCII;
    /**
     * Binary FBX file format, with 7.6.0 version
     */
    public static final FileFormat FBX7600_BINARY;
    /**
     * ASCII FBX file format, with 7.7.0 version
     */
    public static final FileFormat FBX7700ASCII;
    /**
     * Binary FBX file format, with 7.7.0 version
     */
    public static final FileFormat FBX7700_BINARY;

{{< /highlight >}}

Now يمكنك تصدير المشهد إلى FBX 7.6/7.7 في ASCII/وضع البولي B.

Sرمز وافرة:

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid());
    scene.save("fbx7.7.fbx", FileFormat.FBX7700_BINARY);

{{< /highlight >}}


### Added فئة جديدة com.aspose.threed. A3Dptions ptions aveOptions

{{< highlight "java" >}}


/**
 * Save options for A3DW format.
 */
public class A3DWSaveOptions extends SaveOptions
{    
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

    /**
     * If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
     */
    public String getMetaDataPrefix();

    /**
     * If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
     * @param value New value
     */
    public void setMetaDataPrefix(String value);

    /**
     * Constructor of {@link com.aspose.threed.A3DWSaveOptions}
     */
    public A3DWSaveOptions();
}

{{< /highlight >}}

Tانه جديد A3Dptions ptions aveOptions يسمح لك لتصدير معلومات الأصول والخصائص إلى ملف A3DW.

يتم استخدام Tمع بائع الويب الجديد.

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid()).setProperty("rvm:No", "347923");
    var opt = new A3DWSaveOptions();
    opt.setMetaDataPrefix("rvm:");
    scene.save("test.a3dw", opt);

{{< /highlight >}}
