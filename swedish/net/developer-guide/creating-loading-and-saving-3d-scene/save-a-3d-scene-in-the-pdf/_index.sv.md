---
title: Spara en 3D i PDF i C#
linktitle: Spara en 3D i PDF
type: docs
weight: 60
url: /sv/net/save-a-3d-scene-in-the-pdf/
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan bygga en 3D scen genom att lägga till Kamera, Ljus, polygoner och olika andra enheter. De kan nu också spara en 3D-scen i PDF-formatet.
---
##  **Översikt**

Den här artikeln förklarar hur du kan konvertera 3D-fil till PDF-format med C# .NET filhantering och 3D konvertering API, Först behöver du [Ladda 3D fil i sceneobjekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) och sedan spara det i PDF format. Den omfattar ett brett spektrum av ämnen, t.ex.

- Konvertera 3D till PDF i C#
- Konvertera FBX till PDF i C#
- Konvertera STL till PDF i C#
- Konvertera U3D till PDF i C#
- Konvertera OBJ till PDF i C#

{{% alert color="primary" %}} 

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan bygga en 3D scen genom att lägga till Kamera, Ljus, polygoner och olika andra enheter. De kan nu också spara en 3D-scen i PDF-formatet.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET skriver direkt informationen om API och versionsnummer i utdatadokumenten. Till exempel, när en ritning görs till PDF, Aspose. 3D for .NET fyller `Application` med värde 'Aspose. 3D och `PDF Producer` fält med värde, e. 'Aspose. 3D 17,9'.

Observera att du inte kan instruera Aspose.3D for .NET API att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}} 
##  **Skapa en 3D PDF med en cylinder, och renterad i skuggat illustrationsläge med CAD Optimerad belysning**
Metoden Spara i `Scene`-klassen gör det möjligt att spara en 3D-scen i PDF-formatet. Utvecklare kan ladda en 3D-fil som stöds eller bygga en ny 3D-scen, de kan spara en 3D scen i PDF-formatet som visas i detta C# kodexempel:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
