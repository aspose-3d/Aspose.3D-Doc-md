---
title: Variazioni pubbliche di API in Aspose.3D 16.9.0
type: docs
weight: 30
url: /it/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Contenuto sommario**

- [Importa 3D scena dalla fonte PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
-[Aggiunge Aspose.ThreeD.Formats.PdfLoadOptions Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
-[Aggiunge Aspose.ThreeD.FileFormat e Aspose.ThreeD.Formats.PdfFormat Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Salva una scena 3D nel formato PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
-[Aggiunge Aspose.ThreeD.Formats.PdfSaveOptions class e Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Aggiunge il metodo triangolato nella classe Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Aggiunge due metodi BuildTangentBinormal nella classe Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione 2.1.0 alla 16.9.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Importa 3D scena dalla fonte PDF**
Utilizzando la versione recente (16.9.0) o superiore, gli sviluppatori possono recuperare 3D scene da un file PDF inserito.
####  **Aggiunge Aspose.ThreeD.Formats.PdfLoadOptions Class**
Abbiamo aggiunto la classe PdfLoadOptions. Aiuta a caricare il contenuto dal file di input PDF. Gli sviluppatori possono applicare la password per i PDF protetti.

**Apri la scena da un file PDF protetto da password**

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
####  **Aggiunge Aspose.ThreeD.FileFormat e Aspose.ThreeD.Formats.PdfFormat Class**
Abbiamo aggiunto una voce del formato PDF nella classe FileFormat a scopo di caricamento e salvataggio. La classe PdfFormat aiuta a manipolare i PDF.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Estrai tutti i contenuti grezzi da 3D dal file PDF**

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

**Estrai tutte le scene da 3D e salvale in un file FBX**

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
###  **Salva una scena 3D nel formato PDF**
Utilizzando la versione recente (16.9.0) o superiore, gli sviluppatori possono salvare tutti i file 3D supportati nel formato PDF.
####  **Aggiunge Aspose.ThreeD.Formats.PdfSaveOptions class e Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums**
PdfSaveOptions aiuta ad applicare l'impostazione prima di salvare nel formato di output PDF. Gli sviluppatori possono impostare una modalità di rendering e uno schema di illuminazione prima di salvare una scena 3D nel formato PDF come di seguito:

**Crea 3D PDF con un cilindro e renderizzati in modalità illustrazione ombreggiata con illuminazione ottimizzata CAD**

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
###  **Aggiunge il metodo triangolato nella classe Aspose.ThreeD.Entities.PolygonModifier**
Abbiamo aggiunto un altro sovraccarico del metodo Triangulate nella classe PolygonModifier che prende un oggetto classe Scene come parametro.

**Convertire tutti i poligoni in triangoli nel file FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **Aggiunge due metodi BuildTangentBinormal nella classe Aspose.ThreeD.Entities.PolygonModifier**
Abbiamo aggiunto due metodi BuildTangentBinormal nella classe PolygonModifier. Un metodo prende l'oggetto classe Scene come parametro e un altro prende l'oggetto classe Mesh come parametro.

**Costruisci dati tangenti e binormali per tutte le mesh nel file FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
