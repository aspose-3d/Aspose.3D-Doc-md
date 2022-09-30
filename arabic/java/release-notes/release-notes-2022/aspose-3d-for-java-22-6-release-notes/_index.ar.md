---
title: Aspose.3D for Java 22.6 tes elease ootes
type: docs
weight: 7
url: /ar/java/aspose-3d-for-java-22-6-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for Java 22.6.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.6.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1152 |Allow حفظ 3D المشهد دون تحديد تنسيق الملف|New eature|
|THREEDNET-1157 |لا يتم دعم قفل dfdfValueBفي استيراد USDZ|حركة بلا حدود|
|THREEDNET-1156 |GLxcxcxception: غير محدد إلى استيراد glTF ، byteOffset في accessor|إصلاح g ug|
|THREEDNET-1154 |Aspose.ThreeD. ExportEالنقل: duplicpec مكررة في حين DAE إلى USDZ التحويل|إصلاح g ug|
|THREEDNET-1153 |يحدث الحمل أثناء النقل مع توفير USDZ إلى GLTF|إصلاح g ug|



## API التغييرات ##

### Added طريقة جديدة إلى الفئة `com.aspose.threed.FileFormat`:

{{< highlight "csharp" >}}
    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)
{{< /highlight >}}

You يمكن الحصول على instance ileFormat مثيل عن طريق اسم التمديد ، رمز المثال:

{{< highlight "java" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);

{{< /highlight >}}



### Added طريقة جديدة إلى الفئة `com.aspose.threed.Scene`:

{{< highlight "java" >}}
    /**
     * Saves the scene to specified path using specified file format.
     * @param fileName File name.
     */
    public void save(String fileName)
        throws IOException;

{{< /highlight >}}

Tانه طريقة جديدة تسمح لك لحفظ المشهد إلى ملف 3D دون توفير تنسيق الملف.

Eرمز xample:

{{< highlight "java" >}}

var scene = Scene.fromFile("Input.fbx");
scene.save("Output.usdz);

{{< /highlight >}}
