---
title: Offentlig API Ändrar i Aspose.3D 16.11.0
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Innehåll**

- [Adds AddEntity Method in the Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import and Export of glTF Files](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
- [Lägger till Aspose.ThreeD.Formats.GLTFLoadOptions ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)e
- [Lägger till Aspose.ThreeD.Formats.GLTFSaveOptions ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)e
- [Lägger till glTF Format Post i Aspose.ThreeD.FileFormat klass](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)e
- [Lägger till en egenskap för tillägg i Aspose ThreeD.FileFormatType ClassName](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)e
- [Write Dependencies in the Real File System](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
- [Lägger till Aspose.ThreeD.Utilities.DummyFileSystem Class.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)e
- [Lägger till Aspose.ThreeD.Utilities.LocalFileSystem Class.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)e
- [Lägger till Aspose.ThreeD.Utilities.MemoryFileSystem Class.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)e
- [Adds FileSystem property in the Aspose.ThreeD.Formats.IOConfig Class](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 16. 9. 0-16.11. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Lägger tilläggEntity-metoden i Aspose ThreeD.Node Class.**
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
###  **Import och export av glTF Filer**
Genom att använda den senaste versionen (16.11.0) eller högre, kan utvecklare importera och exportera glTF filer till/från andra 3D-filer som stöds.
####  **Lägger till Aspose.ThreeD.Formats.GLTFLoadOptions ClassName**
Vi har lagt till GLTFLoadOptions klass. Det hjälper till att importera glTF-filer till Aspose.3D API.

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
####  **Lägger till Aspose.ThreeD.Formats.GLTFSaveOptions ClassName**
Vi har lagt till GLTFSaveOptions klass. Den definierar inställningar vid sparande av en glTF-fil.

**Inbädda beroenden i utdatan glTF fil**

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

**Skapar en binära glTF fil med KHR_binary_ glTF-ändelsen**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Skapar en binära glTF fil med KHR_binary_ glTF tillsammans med sparningsalternativ**

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
####  **Lägger till glTF Format Post i Aspose.ThreeD.FileFormat klass**
Vi har lagt till poster med GLTF och GLTF_Binary-format för laddning och sparande.
####  **Lägger till en egenskap för tillägg i Aspose ThreeD.FileFormatType ClassName**
Vi har lagt till en Extensions egenskap i FileFormatType-klassen för att få filformatets tilläggsnamn.
###  **Skriv beroende i det verkliga filsystemet**
Genom att använda den senaste versionen (16.11.0) eller högre, kan utvecklare spara alla beroenden 3D i det riktiga filsystemet. Utvecklare kan definiera sökvägen för en lokal katalog, spara i MemoryFileSystem- objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
####  **Lägger till Aspose.ThreeD.Utilities.DummyFileSystem Class.**
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
####  **Lägger till Aspose.ThreeD.Utilities.LocalFileSystem Class.**
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
####  **Lägger till Aspose.ThreeD.Utilities.MemoryFileSystem Class.**
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

byte[] mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
###  **Lägger till egenskapen FileSystem i Aspose.ThreeD.Formats.IOConfig Class.**
Vi har lagt till en FileSystem i IOConfig-klassen för att skriva beroenden.

**Lägger till en FileSystem- egenskap**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
