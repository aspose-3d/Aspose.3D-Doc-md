---
title: Offentlig API Ändrar i Aspose.3D 16.9.0
type: docs
weight: 30
url: /sv/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Innehåll**

- [Import 3D Scene from the Source PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
- [Lägger till Aspose.ThreeD.Formats.PdfLoadOptions ClassName](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)e
- [Lägger till Aspose.ThreeD.FileFormat och Aspose.ThreeD.Formats.PdfFormat Class Class Class.](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)e
- [Save a 3D Scene in the PDF Format](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
- [Lägger till Aspose. 3D. Format. PdfSaveOptions klass och Aspose. 3D. Format. PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)e
- [Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 2.1. 0-16,9. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Importera 3D Scene från källan PDF**
Genom att använda den senaste versionen (16.9.0) eller högre, kan utvecklare hämta 3D scener från en PDF-fil.
####  **Lägger till Aspose.ThreeD.Formats.PdfLoadOptions ClassName**
Vi har lagt till PdfLoadOptions klass. Det hjälper till att ladda innehåll från inmatningsfilen PDF. Utvecklare kan använda lösenord för de skyddade PDF-filerna.

**Öppna scen från en lösenordsskyddad PDF filName**

{{< highlight "java" >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
####  **Lägger till Aspose.ThreeD.FileFormat och Aspose.ThreeD.Formats.PdfFormat Class Class Class.**
Vi har lagt till en post för PDF format i klassen FileFormat för laddning och sparande. PdfFormat-klass hjälper till att manipulera PDF-filer.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extrahera allt obehandlad 3D från filen PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[] content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extrahera alla 3D-scener och spara dem i FBX-filen**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
###  **Spara en 3D Scen i formatet PDF**
Using the recent version (16.9.0) or higher, developers can save all supported 3D files in the PDF format.
####  **Lägger till Aspose. 3D. Format. PdfSaveOptions klass och Aspose. 3D. Format. PdfLightingScheme/PdfRenderMode Enums**
PdfSaveOptions hjälper till att använda inställning innan du sparar i formatet PDF. Utvecklare kan ställa in ett renderingsläge och belysningsschema innan en 3D scen sparas i PDF-formatet som nedan:

**Skapa en 3D PDF med en cylinder, och visat i skuggat illustrationsläge med CAD optimerad belysning**

{{< highlight "java" >}}

 // create a new scene

Scene scene = new Scene();

// create a cylinder child node

scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan)};

// set rendering mode and lighting scheme

PdfSaveOptions opt = new PdfSaveOptions();

opt.LightingScheme = PdfLightingScheme.CAD;

opt.RenderMode = PdfRenderMode.ShadedIllustration;

// save in the PDF format

scene.Save("output.pdf", opt);

{{< /highlight >}}
###  **Lägger till trianguleringsmetoden i Aspose. ThreeD.Entites.PolygonModifier Class.**
Vi har lagt till en annan överbelastning av Triangulate metod i PolygonModifier klassen som tar ett Scene klass objekt som en parameter.

**Konvertera alla polygoner till trianglar i FBX- filen**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **Lägger till två BuildTangentBinormala metoder i Aspose. ThreeD.Entites.PolygonModifier ClassName**
Vi har lagt till två BuildTangentBinormal metoder i PolygonModifier klassen. En metod tar Scene klassobjektet som en parameter och en annan tar Mesh klassobjektet som en parameter.

**Bygg tangens- och binormisk data för alla maskor i filen FBX.**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
