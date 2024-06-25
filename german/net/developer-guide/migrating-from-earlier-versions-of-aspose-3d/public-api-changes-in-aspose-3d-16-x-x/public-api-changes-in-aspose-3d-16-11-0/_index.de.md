---
title: Öffentliche API Änderungen in Aspose.3D 16.11.0
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Inhalts übersicht**

- [Fügt die AddEntity-Methode in der Aspose.ThreeD.Node-Klasse hinzu](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import und Export von glTF Dateien](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
-[Fügt Aspose hinzu. ThreeD. Formate. GLTFLoad Options-Klasse](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
-[Fügt Aspose hinzu. ThreeD. Formate. GLTF SaveOptions-Klasse](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
-[Fügt glTF Format-Eintrag in der Aspose.ThreeD.FileFormat-Klasse hinzu](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
-[Fügt eine Extension-Eigenschaft in der Aspose.ThreeD.FileFormat Type-Klasse hinzu](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Schreiben Sie Abhängigkeiten im realen Dateisystem](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
-[Fügt Aspose hinzu. ThreeD.Utilities.Dummy FileS ystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
-[Fügt Aspose hinzu. ThreeD.Utilities.Local FileSystem-Klasse](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
-[Fügt Aspose hinzu. ThreeD.Utilities.Memory FileS ystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Fügt die FileSystem-Eigenschaft in der Aspose.ThreeD. Formate. IOConfig-Klasse hinzu](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 16.9.0 bis 16.11.0, die für Modul-/Anwendungs entwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
###  **Fügt die AddEntity-Methode in der Aspose.ThreeD.Node-Klasse hinzu**
Eine Abkürzung zum Hinzufügen einer Entität zu einem Knoten.

**Eine Entität zu einem Knoten hinzufügen**

{{< highlight "java" >}}

 // initialize a Scene class object

Scene scene = new Scene();

// create a node

Node sphere = scene.RootNode.CreateChildNode("sphere");

// the old way to add an entity in a node

sphere.Entities.Add(new Sphere());

//the new way to add an entity in a node

sphere.AddEntity(new Sphere());

{{< /highlight >}}
###  **Import und Export von glTF Dateien**
Mit der aktuellen Version (16.11.0) oder höher können Entwickler glTF-Dateien in/aus anderen unterstützten 3D-Dateien importieren und exportieren.
####  **Fügt Aspose hinzu. ThreeD. Formate. GLTFLoad Options-Klasse**
Wir haben die GLTFLoad Options-Klasse hinzugefügt. Es hilft beim Importieren von glTF-Dateien in Aspose.3D API.

**Drehen Sie die V/T-Textur koordination um**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **Fügt Aspose hinzu. ThreeD. Formate. GLTF SaveOptions-Klasse**
Wir haben die GLTF SaveOptions-Klasse hinzugefügt. Es definiert Einstellungen zum Speichern einer glTF-Datei.

**Abhängigkeiten innerhalb der Output glTF-Datei einbetten**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and embed all assets into the target file

// usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders

// use opt.EmbedAssets to tells the aspose.3D to export scene and embed the dependencies inside the target file.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.EmbedAssets = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Verwenden Sie KHR_materials_common Extensions, um die Materialien zu definieren**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Anpassen des Dateinamens der Puffer datei**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Erstellt eine binäre glTF-Datei mit der Erweiterung KHR_binary_glTF**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Erstellt eine binäre glTF-Datei mit der KHR_binary_glTF-Erweiterung zusammen mit den Spar optionen**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension but allow you to configure the save options

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// use saving options

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.Binary);

opt.UseCommonMaterials = true;

// save 3D file

scene.Save("d:\\test.glb", opt);

{{< /highlight >}}
####  **Fügt glTF Format-Eintrag in der Aspose.ThreeD.FileFormat-Klasse hinzu**
Wir haben zum Laden und Speichern Einträge im Format GLTF und GLTF_Binary hinzugefügt.
####  **Fügt eine Extension-Eigenschaft in der Aspose.ThreeD.FileFormat Type-Klasse hinzu**
Wir haben eine Extension-Eigenschaft in der FileFormat Type-Klasse hinzugefügt, um den Erweiterungs namen des Dateiformats zu erhalten.
###  **Schreiben Sie Abhängigkeiten im realen Dateisystem**
Mit der aktuellen Version (16.11.0) oder höher können Entwickler alle 3D Szenen abhängigkeiten im realen Dateisystem speichern. Entwickler können den Pfad eines lokalen Verzeichnisses definieren, im MemoryFileSystem-Objekt speichern oder Abhängigkeiten einfach verwerfen. Die FileSystem-Eigenschaft wird in den Klassen für alle Speicher optionen hinzugefügt.
####  **Fügt Aspose hinzu. ThreeD.Utilities.Dummy FileS ystem Class**
**Speichern der Material dateien verwerfen**

{{< highlight "java" >}}

 // the code example uses the DummyFileSystem, so the material files are not created.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new DummyFileSystem();

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **Fügt Aspose hinzu. ThreeD.Utilities.Local FileSystem-Klasse**
**Abhängigkeiten im lokalen Verzeichnis speichern**

{{< highlight "java" >}}

 // the code example uses the LocalFileSystem class to save dependencies to the local directory.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new LocalFileSystem("E:\\");

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **Fügt Aspose hinzu. ThreeD.Utilities.Memory FileS ystem Class**
**Abhängigkeiten im MemoryFileSystem-Objekt speichern**

{{< highlight "java" >}}

 // the code example uses the MemoryFileSystem to intercepts the dependencies writing.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

MemoryFileSystem mfs = new MemoryFileSystem();

opt.FileSystem = mfs;

// save 3D scene

scene.Save("d:\\test.obj", opt);

//get the test.mtl file content

byte[] mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
###  **Fügt die FileSystem-Eigenschaft in der Aspose.ThreeD. Formate. IOConfig-Klasse hinzu**
Wir haben eine FileSystem-Eigenschaft in der IOConfig-Klasse hinzugefügt, um Abhängigkeiten zu schreiben.

**Fügt eine FileSystem-Eigenschaft hinzu**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
