---
title: Offentlig API Förändringar Aspose.3D 16.11.0
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Innehåll**

- [Lägger till enhetsmetod i Aspose.ThreeD.Nod klass](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import och export av glTF filer](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Lägger till Aspose.ThreeD. Format.GLTFLoadOptions ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.GLTFSaveOptions ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Lägger till glTF Format Post i Aspose.ThreeD.FileFormat Class.](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Lägger till en tilläggsegenskap i Aspose.ThreeD.FileFormatType ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Skriv beroende i det verkliga filsystemet](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Lägger till Aspose.ThreeD.Användare.DummyFileSystem ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Lägger till Aspose.ThreeD.Användare.LokalfilSystem ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Lägger till Aspose.ThreeD.Användningar.MinneFileSystem ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Lägger till egenskapen FileSystem i Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Detta dokument beskriver ändringar i Aspose.3D API från version 16.9. 0-16.11. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteende bakom kulisserna i Aspose.3D.

{{% /alert %}} 
### **Lägger till enhetsmetod i Aspose.ThreeD.Nod klass**
En genväg för att lägga till en enhet i en nod.

**Lägg till en enhet i en nod**

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
### **Import och export av glTF filer**
Använder den senaste versionen (16. 11.0) eller högre, kan utvecklare importera och exportera glTF filer till/från andra stödda 3D filer.
#### **Lägger till Aspose.ThreeD. Format.GLTFLoadOptions ClassName**
Vi har lagt till GLTFLoadOptions klass. Det hjälper till att importera glTF filer till Aspose.3D API.

**Vänd V/T texturkoordinat**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.GLTFSaveOptions ClassName**
Vi har lagt till GLTFSaveOptions klass. Det definierar inställningar för att spara en glTF fil.

**Bädda in beroende inne i utmatningen glTF fil**

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

**Använd KHR_materials_common Extensions för att definiera materialen**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Anpassa bufferfilens filnamn**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Skapar en binär fil glTF med KHR_binary_ glTF- tillägg**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Skapar en binär fil glTF med KHR_binary_glTF- utökning tillsammans med sparalternativ**

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
#### **Lägger till glTF Format Post i Aspose.ThreeD.FileFormat Class.**
Vi har lagt till en GLTF och GLTF_Binary format poster för lastning och sparande.
#### **Lägger till en tilläggsegenskap i Aspose.ThreeD.FileFormatType ClassName**
Vi har lagt till en Extensions egenskap i FileFormatType-klassen för att få filformatets tilläggsnamn.
### **Skriv beroende i det verkliga filsystemet**
Med den senaste versionen (16.11.0) eller högre kan utvecklare spara alla 3D sceneberoenden i det riktiga filsystemet. Utvecklare kan definiera sökvägen för en lokal katalog, spara i MemoryFileSystem- objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
#### **Lägger till Aspose.ThreeD.Användare.DummyFileSystem ClassName**
**Kasta sparande av materialfiler**

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
#### **Lägger till Aspose.ThreeD.Användare.LokalfilSystem ClassName**
**Spara beroende i lokalkatalog**

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
#### **Lägger till Aspose.ThreeD.Användningar.MinneFileSystem ClassName**
**Spara beroende i MemoryFileSystem- objekt**

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
### **Lägger till egenskapen FileSystem i Aspose.ThreeD.Formats.IOConfig**
Vi har lagt till en FileSystem i IOConfig-klassen för att skriva beroenden.

**Lägger till en FileSystem- egenskap**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
