---
title: Aspose.3D ل Python via .NET 22.6 Release Nأوتس
type: docs
weight: 7
url: /ar/python-net/aspose-3d-for-python-net-22-6-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D ل Python via .NET 22.6.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الإصدار ل Aspose.3D ل Python via .NET 22.6.

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

### Added طريقة جديدة إلى الفئة `aspose.threed.FileFormat`

{{< highlight "python" >}}
    
    # Gets the preferred file format from the file extension name
    # The extension name should starts with a dot('.').
    def get_format_by_extension(extensionName)

{{< /highlight >}}

You يمكن الحصول على instance ileFormat مثيل عن طريق اسم التمديد ، رمز المثال:

{{< highlight "python" >}}

scene = Scene(Box())
format = FileFormat.get_format_by_extension(".fbx")
# save the scene to memory stream using FileFormat returned by GetFormatByExtension
stream = BytesIO()
scene.save(stream, format)

{{< /highlight >}}



### Added طريقة جديدة إلى الفئة `aspose.threed.Scene`

{{< highlight "python" >}}

    # Saves the scene to specified path using specified file format.
    def save(fileName)

{{< /highlight >}}

Tانه طريقة جديدة تسمح لك لحفظ المشهد إلى ملف 3D دون توفير تنسيق الملف.

Eرمز xample:

{{< highlight "python" >}}

scene = Scene.from_file("Input.fbx")
scene.save("Output.usdz)

{{< /highlight >}}
