---
title: Import 3D Scenes and Contents from a PDF in C#
linktitle: 3D sahnelerini ve içeriğini PDF 'dan içe aktarın
type: docs
weight: 50
url: /tr/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.
---
{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}}
##  **Bir şifre korumalı PDF açık sahne**
`Scene` sınıfının `Open` yöntemi, 3D sahnesini bir giriş PDF dosyasından yüklemeye izin verir. Geliştiriciler ayrıca bu C# kod örneğinde gösterildiği gibi [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) sınıfını kullanarak korumalı pdf'ler için şifre de uygulayabilir:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Tüm ham 3D içeriğini PDF 'dan ayıklayın**
The Extract method of the [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) class allows to extract 3D contents from a PDF file. Developers may iterate through the contents, and save them into the separate files as shown in this C# code example:

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
##  **Extract All 3D Scenes and Save them into Supported 3D Formats**
`PdfFormat` sınıfının `ExtractScene` yöntemi, PDF dosyasından 3D sahnelerini çıkarmanıza izin verir. Geliştiriciler sahneler aracılığıyla yineleyebilir ve bu C# kod örneğinde gösterildiği gibi desteklenen 3D dosya formatlarında kaydedebilir:

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

Desteklenen tüm 3D dosya biçimleri [Product Overview](/3d/tr/net/product-overview/) sayfasında listelenir.

{{% /alert %}}
