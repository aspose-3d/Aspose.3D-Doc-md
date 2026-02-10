---
title: استورد 3D مشاهد ومحتويات من PDF بـ C#
linktitle: استيراد 3D مشاهد ومحتويات من PDF
type: docs
weight: 50
url: /ar/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.
---
{{% alert color="primary" %}}

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.

{{% /alert %}}
##  **مشهد مفتوح من كلمة مرور محمية PDF**
تسمح طريقة `Open` لفئة `Scene` بتحميل مشهد 3D من ملف إدخال PDF. يمكن للمطورين أيضًا تطبيق كلمة المرور على ملفات pdf المحمية باستخدام فئة [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) كما هو موضح في مثال رمز C# هذا:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **استخراج جميع محتويات 3D الخام من PDF**
تسمح طريقة الاستخراج لفئة [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) باستخراج محتويات 3D من ملف PDF. يمكن للمطورين تكرار المحتويات وحفظها في الملفات المنعزلة كما هو موضح في مثال رمز C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
byte[] password = null;
// Extract 3D contents
List<byte[]> contents = FileFormat.PDF.Extract("House_Design.pdf", password);
int i = 1;
// Iterate through the contents and in separate 3D files
foreach (byte[] content in contents)
{
    string fileName = "3d-" + (i++);
    File.WriteAllBytes(fileName, content);
}

{{< /highlight >}}
##  **استخرج جميع مشاهد 3D وحفظها في تنسيقات 3D المدعومة**
The `ExtractScene` method of the `PdfFormat` class allows to extract 3D scenes from a PDF file. Developers may iterate through the scenes, and save them in the supported 3D file formats as shown in this C# code example:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            byte[] password = null;
            List<Scene> scenes = FileFormat.PDF.ExtractScene("House_Design.pdf", password);
            int i = 1;
            // Iterate through the scenes and save in 3D files
            foreach (Scene scene in scenes)
            {
                string fileName = "3d-" + (i++) + ".fbx";
                scene.Save(RunExamples.GetOutputFilePath(fileName), FileFormat.FBX7400ASCII);
            }

{{< /highlight >}}

{{% alert color="primary" %}}

جميع تنسيقات الملفات المدعومة 3D مدرجة في صفحة [Roرودوكت Oفيرفيو](/3d/ar/net/product-overview/).

{{% /alert %}}
