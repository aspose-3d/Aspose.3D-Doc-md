---
title: Aspose 中的公共 API 更改。3D 16.11.0
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-16-11-0/
---
**内容摘要**

- [在 Aspose.ThreeD.Node类中添加AddEntity方法](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [glTF 文件的导入和导出](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
-[添加 Aspose.ThreeD.Formats.GLTFLoadOptions类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
-[添加 Aspose.ThreeD.Formats.GLTFSaveOptions类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
-[在 Aspose.ThreeD.FileFormat类中添加 glTF 格式项](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
-[在 Aspose.ThreeD.FileFormatType类中添加扩展属性](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [在真实文件系统中写入依赖关系](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
-[添加 Aspose.ThreeD.Utilities.DummyFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
-[添加 Aspose.ThreeD.Utilities.LocalFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
-[添加 Aspose.ThreeD.Utilities.MemoryFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [在 Aspose.ThreeD.Formats.IOConfig类中添加FileSystem属性](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

本文档介绍了模块/应用程序开发人员可能感兴趣的对 Aspose.3D API 从版本16.9.0到16.11.0的更改。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **在 Aspose.ThreeD.Node类中添加AddEntity方法**
将实体添加到节点的快捷方式。

**将实体添加到节点**

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
###  **glTF 文件的导入和导出**
使用最新版本 (16.11.0) 或更高版本，开发人员可以将 glTF 文件导入和导出到其他受支持的 3D 文件。
####  **添加 Aspose.ThreeD.Formats.GLTFLoadOptions类**
我们添加了GLTFLoadOptions类。它有助于将 glTF 文件导入 Aspose.3D API。

**翻转V/T纹理坐标**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.GLTFSaveOptions类**
我们添加了GLTFSaveOptions类。它定义了保存 glTF 文件的设置。

**在输出 glTF 文件中嵌入依赖项**

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

**使用KHR_materials_common Extensions定义材质**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**自定义缓冲区文件的文件名**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**使用KHR_binary_glTF扩展名创建二进制 glTF 文件**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**使用KHR_binary_glTF扩展名以及保存选项创建二进制 glTF 文件**

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
####  **在 Aspose.ThreeD.FileFormat类中添加 glTF 格式项**
我们添加了 GLTF 和GLTF_Binary格式条目，用于加载和保存目的。
####  **在 Aspose.ThreeD.FileFormatType类中添加扩展属性**
我们在FileFormatType类中添加了扩展名属性，以获取文件格式的扩展名名称。
###  **在真实文件系统中写入依赖关系**
使用最新版本 (16.11.0) 或更高版本，开发人员可以将所有 3D 场景依赖项保存在真实文件系统中。开发人员可以定义本地目录的路径，保存在MemoryFileSystem对象中或简单地丢弃依赖项。在all save选项类中添加了FileSystem属性。
####  **添加 Aspose.ThreeD.Utilities.DummyFileSystem类**
**放弃保存材料文件**

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
####  **添加 Aspose.ThreeD.Utilities.LocalFileSystem类**
**在本地目录中保存依赖项**

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
####  **添加 Aspose.ThreeD.Utilities.MemoryFileSystem类**
**在MemoryFileSystem对象中保存依赖关系**

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
###  **在 Aspose.ThreeD.Formats.IOConfig类中添加FileSystem属性**
我们在IOConfig类中添加了一个文件系统属性来编写依赖项。

**添加文件系统属性**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
