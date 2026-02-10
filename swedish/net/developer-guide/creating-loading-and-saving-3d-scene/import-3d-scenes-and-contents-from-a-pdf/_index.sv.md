---
title: Importera 3D Scener och innehåll från en PDF i C#
linktitle: Importera 3D Scener och innehåll från en PDF
type: docs
weight: 50
url: /sv/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.
---
{{% alert color="primary" %}}

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.

{{% /alert %}}
##  **Open Scene from a Password Protected PDF**
`Open`-metoden för `Scene`-klassen tillåter att ladda 3D-scenen från en inmatningsfil PDF. Utvecklare kan också använda lösenord för de skyddade PDF-filerna med [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) klassen som visas i detta C# kodexempel:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Extrahera alla obehandlade 3D Innehåll från en PDF**
Utdragsmetoden för [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) gör det möjligt att dra ut 3D innehåll från en PDF-fil. Utvecklare kan itera genom innehållet, och spara dem i de separata filerna som visas i detta C# kodexempel:

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
##  **Extrahera alla 3D Scener och spara dem i format som stöds 3D**
`ExtractScene`-metoden för `PdfFormat`-klassen tillåter att extrahera 3D scener från en PDF-fil. Utvecklare kan itera genom scenerna, och spara dem i de 3D filformat som stöds som visas i detta C# kodexempel:

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
