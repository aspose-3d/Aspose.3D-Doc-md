---
title: Importer 3D Scènes et contenu d'un PDF dans C#
linktitle: Importer 3D Scènes et contenus d'un PDF
type: docs
weight: 50
url: /fr/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: La classe Scene de Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire des scènes 3D et le contenu d'un fichier PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la scène Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire 3D scènes et le contenu d'un fichier PDF.

{{% /alert %}}
##  **Ouvrir une scène à partir d'un mot de passe protégé PDF**
La méthode `Open` de la classe `Scene` permet de charger la scène 3D à partir d'un fichier d'entrée PDF. Les développeurs peuvent également appliquer un mot de passe pour les PDF protégés en utilisant la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) comme indiqué dans cet exemple de code C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Extraire tout le contenu brut 3D d'un PDF**
La méthode Extract de la classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permet d'extraire le contenu 3D d'un fichier PDF. Les développeurs peuvent parcourir le contenu et les enregistrer dans les fichiers séparés comme indiqué dans cet exemple de code C#:

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
##  **Extraire toutes les scènes 3D et les enregistrer dans les formats 3D pris en charge**
La méthode `ExtractScene` de la classe `PdfFormat` permet d'extraire des scènes 3D d'un fichier PDF. Les développeurs peuvent parcourir les scènes et les enregistrer dans les formats de fichier 3D pris en charge, comme indiqué dans cet exemple de code C#:

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

Tous les formats de fichier 3D pris en charge sont répertoriés dans la page [Aperçu du produit](/3d/fr/net/product-overview/).

{{% /alert %}}
