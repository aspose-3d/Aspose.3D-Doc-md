---
title: Import 3D Scenes and Contents from a PDF in C#
linktitle: Import 3D Scenes and Contents from a PDF
type: docs
weight: 50
url: /net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.
---

{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}}
## **Open Scene from a Password Protected PDF**
The `Open` method of the `Scene` class allows to load the 3D scene from an input PDF file. Developers may also apply password for the protected PDFs using [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) class as shown in this C# code example:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
## **Extract All Raw 3D Contents from a PDF**
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
## **Extract All 3D Scenes and Save them into Supported 3D Formats**
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

All the supported 3D file formats are listed in the [Product Overview](/3d/net/product-overview/) page.

{{% /alert %}}
