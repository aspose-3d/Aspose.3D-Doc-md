---
title: Aspose.3D中的公共API变化16.11.0
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-16-11-0/
---
**内容摘要**

- [在Aspose.ThreeD.Node类中添加AddEntity方法](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [导入和导出glTF文件](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [添加Aspose.ThreeD.Formats.Gltfloadoptons类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [添加Aspose.ThreeD.Formats.GLTFSaveOptions类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [在Aspose.ThreeD.FileFormat类中添加glTF格式条目](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [在Aspose.ThreeD.Fileforgatype类中添加扩展属性](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [在真实文件系统中写入依赖关系](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [添加Aspose.ThreeD.Utilities.DummyFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [添加Aspose.ThreeD.Utilities.LocalFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [添加Aspose.ThreeD.实用程序.MemoryFileSystem类](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [在Aspose.ThreeD.Formats.IOConfig类中添加FileSystem属性](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

本文档介绍了从版本16.9.0到16.11.0的Aspose.3D API的更改，这些更改可能是模块/应用程序开发人员感兴趣的。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
### **在Aspose.ThreeD.Node类中添加AddEntity方法**
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
### **导入和导出glTF文件**
使用最新版本 (16.11.0) 或更高版本，开发人员可以将glTF文件导入或导出其他受支持的3D文件。
#### **添加Aspose.ThreeD.Formats.Gltfloadoptons类**
我们添加了gltfloadopions类。它有助于将glTF文件导入Aspose.3D API。

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
#### **添加Aspose.ThreeD.Formats.GLTFSaveOptions类**
我们添加了GLTFSaveOptions类。它定义保存glTF文件时的设置。

**将依赖项嵌入到输出glTF文件中**

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

**使用KHR_binary_glTF扩展名创建二进制glTF文件**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**使用KHR_binary_glTF扩展以及保存选项创建二进制glTF文件**

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
#### **在Aspose.ThreeD.FileFormat类中添加glTF格式条目**
为了加载和保存的目的，我们添加了GLTF和GLTF的二进制格式条目。
#### **在Aspose.ThreeD.Fileforgatype类中添加扩展属性**
我们在FileFormatType类中添加了扩展名属性，以获取文件格式的扩展名名称。
### **在真实文件系统中写入依赖关系**
使用最新版本 (16.11.0) 或更高版本，开发人员可以将所有3D场景依赖项保存在真实文件系统中。开发人员可以定义本地目录的路径，保存在MemoryFileSystem对象中，或者只是丢弃依赖项。文件系统属性被添加到所有保存选项类中。
#### **添加Aspose.ThreeD.Utilities.DummyFileSystem类**
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
#### **添加Aspose.ThreeD.Utilities.LocalFileSystem类**
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
#### **添加Aspose.ThreeD.实用程序.MemoryFileSystem类**
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

byte[]mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
### **在Aspose.ThreeD.Formats.IOConfig类中添加FileSystem属性**
我们在IOConfig类中添加了一个文件系统属性来编写依赖项。

**添加文件系统属性**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
