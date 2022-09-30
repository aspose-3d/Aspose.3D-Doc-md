---
title: Public API Changes Aspose.3D 16.11.0
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Contents Summary**

- [Aspose.ThreeD.Node lass lass içinde dds dds ddddEntity ethethod](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import ve Export glTF Files](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Dds dds Aspose.ThreeD.Formats. Glass lass lass ooadlass ptions lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. Glass lass aveavelass ptions lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Dds dds glTF Format try ntry Aspose.ThreeD.FileFormat lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Dds dds Aspose.ThreeD. Filelass ormatlass ype lass lass bir Extension özelliği](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Real pendenpendeneal in the eal eal File System](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Dds dds Aspose.ThreeD.Utilities. Dummyumilestem ystem lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Dds dds Aspose.ThreeD.Utilities. Locallass ilestem ystem lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Dds dds Aspose.ThreeD. lities tilities.MemoryFileSystem lass lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Aspose.ThreeD.Formats. Ionononfig lass property içinde dds dds Filestem ystem özelliği](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Tbelge, 16.9.0 sürümünden 16.11.0 'a kadar Aspose.3D API 'teki değişiklikleri açıklar, bu da modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Aspose.ThreeD.Node lass lass içinde dds dds ddddEntity ethethod**
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
### **Import ve Export glTF Files**
Developers son sürümü (16.11.0) veya daha yüksek şarkı söyleyen geliştiriciler glTF dosyalarını diğer desteklenen 3D dosyalarına aktarabilir ve aktarabilir.
#### **Dds dds Aspose.ThreeD.Formats. Glass lass lass ooadlass ptions lass lass**
We Gptions TFLptions oadptions ptions class ekledi. It glTF dosyalarını Aspose.3D API dosyasına aktarmaya yardımcı olur.

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
#### **Dds dds Aspose.ThreeD.Formats. Glass lass aveavelass ptions lass lass**
We, GLTaveaveaveaveptions class ekledi. It, glTF dosyasını kaydetme ayarlarını tanımlar.

**EDDependenpendenside nside the ututput glTF File**

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

**Creates a Binary glTF File KHR_binary_glTF tension xtension kullanarak**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**CSaving ptions ptions ile birlikte 07Extension kullanarak glTF File bir Binary reates**

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
#### **Dds dds glTF Format try ntry Aspose.ThreeD.FileFormat lass lass**
We, yükleme ve kaydetme amaçlı GLTF ve GLTF_Binary format girişlerini eklemiştir.
#### **Dds dds Aspose.ThreeD. Filelass ormatlass ype lass lass bir Extension özelliği**
Dosya biçiminin uzantısı adını almak için File. ormat. ype sınıfında bir Extension özelliği ekledik.
### **Real pendenpendeneal in the eal eal File System**
Developers son sürümü (16.11.0) veya daha yüksek, geliştiriciler gerçek dosya sisteminde 3D sahne bağımlılıklarını kaydedebilir. Developers, yerel bir dizinin yolunu tanımlayabilir, MemoryFileSystem nesnesine kaydedebilir veya sadece bağımlılıkları atabilir. The Filestem ystem özelliği tüm kaydetme seçeneği sınıflarına eklenir.
#### **Dds dds Aspose.ThreeD.Utilities. Dummyumilestem ystem lass lass**
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
#### **Dds dds Aspose.ThreeD.Utilities. Locallass ilestem ystem lass lass**
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
#### **Dds dds Aspose.ThreeD. lities tilities.MemoryFileSystem lass lass**
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

byte[]mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
### **Aspose.ThreeD.Formats. Ionononfig lass property içinde dds dds Filestem ystem özelliği**
We, bağımlılıkları yazmak için Ifig fig onfig sınıfında bir File. ystem özelliği eklemiştir.

**Dds dds a stem ilestem ystem özelliği**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
