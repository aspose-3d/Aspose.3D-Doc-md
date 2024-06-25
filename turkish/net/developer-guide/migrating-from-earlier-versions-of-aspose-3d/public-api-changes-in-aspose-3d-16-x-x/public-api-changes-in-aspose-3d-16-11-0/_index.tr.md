---
title: Kamu API Aspose içinde değişir. 3D 16.11.0
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Contents Summary**

- [Addentity yöntemini Aspose. threed. node sınıfında ekler](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import and Export of glTF Files](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
-[Aspose ekler. threed. formats. gltfloadoptions sınıfı](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
-[Aspose ekler. threed. formats. gltfsaveoptions sınıfı](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
-[Adds glTF Format Entry in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
-[Adds an Extension property in the Aspose.ThreeD.FileFormatType Class](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Real pendenpendeneal in the eal eal File System](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
-[Aspose ekler. threed. yardımcı programlar. dummyfilesystem sınıfı](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
-[Aspose ekler. threed. yardımcı programlar. localfilesystem sınıfı](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
-[Aspose ekler. threed. yardımcı programlar. memoryfilesystem sınıfı](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Dosya sistemi özelliğini Aspose. threed. formats. ioconfig sınıfında ekler](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.9.0 to 16.11.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Addentity yöntemini Aspose. threed. node sınıfında ekler**
Bir düğüme bir varlık eklemek için shortcut kısayol yolu.

**Ndd bir Node için bir Entity**

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
###  **Import and Export of glTF Files**
Using the recent version (16.11.0) or higher, developers can import and export glTF files to/from other supported 3D files.
####  **Aspose ekler. threed. formats. gltfloadoptions sınıfı**
We have added GLTFLoadOptions class. It helps in importing glTF files into Aspose.3D API.

**Lip lip V/T Texture ordinoordinate**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **Aspose ekler. threed. formats. gltfsaveoptions sınıfı**
Gltfsaveoptions sınıfını ekledik. glTF dosyasını kaydetme ayarlarını tanımlar.

**Çıktı glTF dosyasının içine bağımlılıklar yerleştirildi**

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

**Mse K___materials_common Mxtensions to Mefine the Materials**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Bustomize Buffer ffer ile**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Khr_binary_gltf uzantısını kullanarak ikili glTF dosyası oluşturur**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Tasarruf seçenekleri ile birlikte khr_binary_gltf uzantısını kullanarak ikili glTF dosyası oluşturur**

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
####  **Adds glTF Format Entry in the Aspose.ThreeD.FileFormat Class**
We have added a GLTF and GLTF_Binary format entries for loading and saving purposes.
####  **Adds an Extension property in the Aspose.ThreeD.FileFormatType Class**
Dosya biçiminin uzantısı adını almak için File. ormat. ype sınıfında bir Extension özelliği ekledik.
###  **Real pendenpendeneal in the eal eal File System**
Son sürümü (16.11.0) veya daha yüksek kullanarak, geliştiriciler gerçek dosya sisteminde tüm 3D sahne bağımlılıklarını kaydedebilir. Geliştiriciler yerel bir dizinin yolunu tanımlayabilir, memoryfilesystem nesnesine kaydedebilir veya sadece bağımlılıkları atabilirler. Dosya sistemi özelliği tüm kaydetme seçeneği sınıflarına eklenir.
####  **Aspose ekler. threed. yardımcı programlar. dummyfilesystem sınıfı**
**Erial iscard erial aving erial aterial Files**

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
####  **Aspose ekler. threed. yardımcı programlar. localfilesystem sınıfı**
**Local Directory içinde Dave pendenependencies**

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
####  **Aspose ekler. threed. yardımcı programlar. memoryfilesystem sınıfı**
**MemoryFileSystem MemoryFileSystem bject'de pendenave pendenependencies**

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
###  **Dosya sistemi özelliğini Aspose. threed. formats. ioconfig sınıfında ekler**
We, bağımlılıkları yazmak için Ifig fig onfig sınıfında bir File. ystem özelliği eklemiştir.

**Dds dds a stem ilestem ystem özelliği**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
