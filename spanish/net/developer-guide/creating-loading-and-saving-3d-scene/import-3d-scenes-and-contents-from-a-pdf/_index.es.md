---
title: Importar 3D escenas y contenidos de un PDF en C#
linktitle: Importar 3D escenas y contenidos desde un PDF
type: docs
weight: 50
url: /es/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: La clase Scene de Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.
---
{{% alert color="primary" %}}

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.

{{% /alert %}}
##  **Abrir escena desde una contraseña protegida PDF**
El método `Open` de la clase `Scene` permite cargar la escena 3D desde un archivo PDF de entrada. Los desarrolladores también pueden aplicar una contraseña para los PDF protegidos usando la clase [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) como se muestra en este ejemplo de código C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Extraer todo el contenido Raw 3D de un PDF**
El método Extract de la clase [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permite extraer el contenido 3D de un archivo PDF. Los desarrolladores pueden iterar a través de los contenidos y guardarlos en los archivos separados como se muestra en este ejemplo de código C#:

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
##  **Extraer todas las escenas 3D y guardarlas en formatos 3D compatibles**
El método `ExtractScene` de la clase `PdfFormat` permite extraer escenas 3D de un archivo PDF. Los desarrolladores pueden iterar a través de las escenas y guardarlas en los formatos de archivo 3D compatibles como se muestra en este ejemplo de código C#:

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

Todos los formatos de archivo 3D admitidos se enumeran en la página [Descripción general del producto](/3d/es/net/product-overview/).

{{% /alert %}}
