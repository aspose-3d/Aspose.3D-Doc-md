---
title: Pubblico API Modifiche nel Aspose.3D 16.11.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Contenuto sommario**

- [Aggiunge il metodo di entità nella classe Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Importazione ed esportazione di glTF file](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Aggiunge Aspose.ThreeD.Formats.GLTFLoadOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Aggiunge Aspose.ThreeD.Formats.GLTFSaveOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Aggiunge la voce del formato glTF nella classe Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Aggiunge una proprietà Extension nella classe Aspose.ThreeD.FileFormatType](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Scrivi dipendenze nel file system reale](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Aggiunge Aspose.ThreeD.Utilities.DummyFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Aggiunge Aspose.ThreeD.Utilities.LocalFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Aggiunge Aspose.ThreeD.Utilities.MemoryFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Aggiunge la proprietà FileSystem nella classe Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.3D API dalla versione 16.9.0 alla 16.11.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte nello Aspose.3D.

{{% /alert %}} 
### **Aggiunge il metodo di entità nella classe Aspose.ThreeD.Node**
Un modo di scelta rapida per l'aggiunta di un'entità a un nodo.

**Aggiungere un'entità a un nodo**

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
### **Importazione ed esportazione di glTF file**
Utilizzando la versione recente (16.11.0) o superiore, gli sviluppatori possono importare ed esportare i file glTF in/da altri file 3D supportati.
#### **Aggiunge Aspose.ThreeD.Formats.GLTFLoadOptions Class**
Abbiamo aggiunto la classe GLTFLoadOptions. Aiuta a importare i file glTF in Aspose.3D API.

**Capovolgi la Coordinata texture V/T**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
#### **Aggiunge Aspose.ThreeD.Formats.GLTFSaveOptions Class**
Abbiamo aggiunto la classe GLTFSaveOptions. Definisce le impostazioni sul salvataggio di un file glTF.

**Incorporare le dipendenze all'interno del file di output glTF**

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

**Utilizzare le estensioni KHR_materials_common per definire i materiali**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Personalizzare il nome del file Buffer**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Crea un file binario glTF utilizzando l'estensione KHR_binary_glTF**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Crea un file binario glTF utilizzando l'estensione KHR_binary_glTF insieme alle opzioni di salvataggio**

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
#### **Aggiunge la voce del formato glTF nella classe Aspose.ThreeD.FileFormat**
Abbiamo aggiunto un GLTF e GLTF_Formato binario voci per il caricamento e il salvataggio.
#### **Aggiunge una proprietà Extension nella classe Aspose.ThreeD.FileFormatType**
Abbiamo aggiunto una proprietà Extension nella classe FileFormatType per ottenere il nome dell'estensione del formato del file.
### **Scrivi dipendenze nel file system reale**
Utilizzando la versione recente (16.11.0) o superiore, gli sviluppatori possono salvare tutte le dipendenze della scena 3D nel file system reale. Gli sviluppatori possono definire il percorso di una directory locale, salvare nell'oggetto MemoryFileSystem o semplicemente scartare le dipendenze. La proprietà FileSystem viene aggiunta nelle classi di tutte le opzioni di salvataggio.
#### **Aggiunge Aspose.ThreeD.Utilities.DummyFileSystem Class**
**Scartare il salvataggio dei file materiali**

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
#### **Aggiunge Aspose.ThreeD.Utilities.LocalFileSystem Class**
**Salvare le dipendenze nella directory locale**

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
#### **Aggiunge Aspose.ThreeD.Utilities.MemoryFileSystem Class**
**Salvare le dipendenze nell'oggetto MemoryFileSystem**

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

byte[]mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
### **Aggiunge la proprietà FileSystem nella classe Aspose.ThreeD.Formats.IOConfig**
Abbiamo aggiunto una proprietà FileSystem nella classe IOConfig per scrivere dipendenze.

**Aggiunge una proprietà FileSystem**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
