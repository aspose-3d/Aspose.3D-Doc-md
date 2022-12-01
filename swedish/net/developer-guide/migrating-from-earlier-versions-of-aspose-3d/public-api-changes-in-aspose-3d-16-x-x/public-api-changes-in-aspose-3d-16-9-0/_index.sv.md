---
title: Offentlig API Förändringar under Aspose.3D 16,9,0
type: docs
weight: 30
url: /sv/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Innehåll**

- [Import 3D Scen från källan PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Lägger till Aspose.ThreeD. Format.PdfLoadOptions ClassName](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Lägger till Aspose.ThreeD.FileFormat och Aspose.ThreeD. Format.PdfFormat klass](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Spara en 3D scen i formatet PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Lägger till Aspose.ThreeD. Format. PdfSaveOptions klass och Aspose.ThreeD. Format. PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Lägger till Trianguleringsmetod i Aspose.ThreeD.Entites.PolygonModifier Class.](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Lägger till två BuildTangentBinormala metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Detta dokument beskriver ändringar i Aspose.3D API från version 2.1. 0-16,9. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteende bakom kulisserna i Aspose.3D.

{{% /alert %}} 
### **Import 3D Scen från källan PDF**
Använder den senaste versionen (16. 9.0) eller högre, kan utvecklare hämta 3D scener från en indata PDF fil.
#### **Lägger till Aspose.ThreeD. Format.PdfLoadOptions ClassName**
Vi har lagt till PdfLoadOptions klass. Det hjälper till att ladda innehåll från indata PDF-filen. Utvecklare kan använda lösenord för de skyddade PDF-filerna.

**Öppen scen från en lösenordsskyddad PDF-fil.**

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
#### **Lägger till Aspose.ThreeD.FileFormat och Aspose.ThreeD. Format.PdfFormat klass**
Vi har lagt till en post av PDF format i FileFormat klassen för lastning och sparande. PdfFormat-klass hjälper till att manipulera PDF-filer.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extrahera all rå 3D innehåll från PDF fil.**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[]content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extrahera alla 3D scener och spara dem i FBX filer**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
### **Spara en 3D scen i formatet PDF**
Med den senaste versionen (16.9.0) eller högre kan utvecklare spara alla 3D-filer som stöds i formatet PDF.
#### **Lägger till Aspose.ThreeD. Format. PdfSaveOptions klass och Aspose.ThreeD. Format. PdfLightingScheme/PdfRenderMode Enums**
PdfSaveOptions hjälper till att tillämpa inställning innan du sparar i utgången PDF-formatet. Utvecklare kan ställa in ett renderingsläge och belysningsschema innan de sparar en 3D scen i formatet PDF Nedan:

**Skapa en 3D PDF med en cylinder, och återgivna i skuggad illustration med CAD optimerad belysning**

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
### **Lägger till Trianguleringsmetod i Aspose.ThreeD.Entites.PolygonModifier Class.**
Vi har lagt till en annan överbelastning av Triangulate metod i PolygonModifier klassen som tar ett Scene klass objekt som en parameter.

**Konvertera alla polygoner till trianglar i filen FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Lägger till två BuildTangentBinormala metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.**
Vi har lagt till två BuildTangentBinormal metoder i PolygonModifier klassen. En metod tar Scene klassobjektet som en parameter och en annan tar Mesh klassobjektet som en parameter.

**Bygg tangens och kikare för alla maskor i filen FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
