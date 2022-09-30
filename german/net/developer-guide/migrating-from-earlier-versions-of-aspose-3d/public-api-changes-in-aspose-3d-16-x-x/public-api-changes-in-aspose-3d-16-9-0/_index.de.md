---
title: Öffentliche API Änderungen in Aspose.3D 16.9.0
type: docs
weight: 30
url: /de/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Inhalts übersicht**

- [Szene aus der Quelle PDF Import 3D](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Fügt Aspose.ThreeD. Formate. PdfLoad Options-Klasse hinzu](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Fügt Aspose.ThreeD.File Format und Aspose.ThreeD hinzu. Formate. PdfFormat-Klasse](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Speichern Sie eine 3D Szene im Format PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Fügt Aspose.ThreeD. Formate. PdfSaveOptions-Klasse und Aspose.ThreeD hinzu. Formate. Pdf Lighting Scheme/PdfRender Mode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Fügt die Triangulate-Methode in der Aspose.ThreeD. Entitäten. Polygonmodifier-Klasse hinzu](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Fügt der Aspose.ThreeD.Entities.Polygon Modifier Class zwei Build Tangent Binormal-Methoden hinzu](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an der Aspose.3D API von Version 2.1.0 bis 16.9.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Szene aus der Quelle PDF Import 3D**
Mit der aktuellen Version (16.9.0) oder höher können Entwickler 3D Szenen aus einer Eingabe PDF-Datei abrufen.
#### **Fügt Aspose.ThreeD. Formate. PdfLoad Options-Klasse hinzu**
Wir haben die PdfLoad Options-Klasse hinzugefügt. Es hilft beim Laden von Inhalten aus der Datei Input PDF. Entwickler können ein Passwort für die geschützten PDFs anwenden.

**Öffnen Sie die Szene aus einer passwort geschützten Datei PDF**

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
#### **Fügt Aspose.ThreeD.File Format und Aspose.ThreeD hinzu. Formate. PdfFormat-Klasse**
Wir haben einen Eintrag im Format PDF in der FileFormat-Klasse zum Laden und Speichern hinzugefügt. Die PdfFormat-Klasse hilft bei der Manipulation von PDFs.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extrahieren Sie alle Roh inhalte 3D aus der Datei PDF**

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

**Extrahieren Sie alle Szenen 3D und speichern Sie sie in der Datei FBX**

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
### **Speichern Sie eine 3D Szene im Format PDF**
Mit der aktuellen Version (16.9.0) oder höher können Entwickler alle unterstützten 3D-Dateien im Format PDF speichern.
#### **Fügt Aspose.ThreeD. Formate. PdfSaveOptions-Klasse und Aspose.ThreeD hinzu. Formate. Pdf Lighting Scheme/PdfRender Mode Enums**
Die PdfSaveOptions hilft bei der Anwendung der Einstellung vor dem Speichern im Ausgabe format PDF. Entwickler können einen Rendering-Modus und ein Beleuchtungs schema festlegen, bevor sie eine 3D-Szene wie folgt im Format PDF speichern:

**Erstellen Sie eine 3D PDF mit einem Zylinder und gerendert im schattierten Illustration modus mit CAD optimierter Beleuchtung**

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
### **Fügt die Triangulate-Methode in der Aspose.ThreeD. Entitäten. Polygonmodifier-Klasse hinzu**
Wir haben eine weitere Überladung der Triangulate-Methode in der PolygonModifier-Klasse hinzugefügt, die ein Scene-Klassen objekt als Parameter verwendet.

**Konvertieren Sie alle Polygone in Dreiecke in der Datei FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Fügt der Aspose.ThreeD.Entities.Polygon Modifier Class zwei Build Tangent Binormal-Methoden hinzu**
Wir haben zwei Build Tangentbinormal-Methoden in der PolygonModifier-Klasse hinzugefügt. Eine Methode verwendet das Scene-Klassen objekt als Parameter und eine andere das Mesh-Klassen objekt als Parameter.

**Tangente und binormale Daten für alle Maschen in der Datei FBX erstellen**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
