---
title: Aspose.3D for .NET 22.6 tes elease ootes
type: docs
weight: 7
url: /ar/net/aspose-3d-for-net-22-6-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for .NET 22.6.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.6.

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



### Added طريقة جديدة إلى الفئة `Aspose.ThreeD.FileFormat`

{{< highlight "csharp" >}}

    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)

{{< /highlight >}}

You يمكن الحصول على instance ileFormat مثيل عن طريق اسم التمديد ، رمز المثال:

{{< highlight "csharp" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);


{{< /highlight >}}



### Added طريقة جديدة إلى الفئة `Aspose.ThreeD.Scene`

{{< highlight "csharp" >}}
        /// <summary>
        /// Saves the scene to specified path using specified file format.
        /// </summary>
        /// <param name="fileName">File name.</param>
        public void Save(string fileName)
{{< /highlight >}}

Tانه طريقة جديدة تسمح لك لحفظ المشهد إلى ملف 3D دون توفير تنسيق الملف.

Eرمز xample:

{{< highlight "csharp" >}}

var scene = Scene.FromFile("Input.fbx");
scene.Save("Output.usdz);

{{< /highlight >}}


### Added طرق جديدة إلى الفئة `Aspose.ThreeD.Transform`

{{< highlight "csharp" >}}
        public Transform SetGeometricTranslation(double x, double y, double z)
        public Transform SetGeometricScaling(double sx, double sy, double sz)
        public Transform SetGeometricRotation(double rx, double ry, double rz)
        public Transform SetTranslation(double tx, double ty, double tz)
        public Transform SetScale(double sx, double sy, double sz)
        public Transform SetEulerAngles(double rx, double ry, double rz)
        public Transform SetRotation(double rw, double rx, double ry, double rz)
        public Transform SetPreRotation(double rx, double ry, double rz)
        public Transform SetPostRotation(double rx, double ry, double rz)
{{< /highlight >}}

يتم توفير أساليب المساعد hese for Java/Python الربط ، يمكنك أيضا استخدامها لتوفير التحول على غرار سلسلة ، رمز المثال:


{{< highlight "csharp" >}}
        var scene = new Scene();
        var node = scene.RootNode.CreateChildNode(new Box());
        node.Transform
                .SetTranslation(10, 0, 0)
                .SetScale(20, 1, 1)
        ;
{{< /highlight >}}
