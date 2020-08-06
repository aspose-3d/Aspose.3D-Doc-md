---
title: Public API Changes in Aspose.3D 16.11.0
type: docs
weight: 20
url: /net/public-api-changes-in-aspose-3d-16-11-0/
---

**Contents Summary**

- [Adds AddEntity Method in the Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import and Export of glTF Files](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Adds Aspose.ThreeD.Formats.GLTFLoadOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.GLTFSaveOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Adds glTF Format Entry in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Adds an Extension property in the Aspose.ThreeD.FileFormatType Class](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Write Dependencies in the Real File System](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Adds Aspose.ThreeD.Utilities.DummyFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Adds Aspose.ThreeD.Utilities.LocalFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Adds Aspose.ThreeD.Utilities.MemoryFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Adds FileSystem property in the Aspose.ThreeD.Formats.IOConfig Class](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.9.0 to 16.11.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Adds AddEntity Method in the Aspose.ThreeD.Node Class**
A shortcut way for adding an entity to a node.

**Add an Entity to a Node**

{{< highlight java >}}

 // initialize a Scene class object

Scene scene = new Scene();

// create a node

Node sphere = scene.RootNode.CreateChildNode("sphere");

// the old way to add an entity in a node

sphere.Entities.Add(new Sphere());

//the new way to add an entity in a node

sphere.AddEntity(new Sphere());

{{< /highlight >}}
### **Import and Export of glTF Files**
Using the recent version (16.11.0) or higher, developers can import and export glTF files to/from other supported 3D files.
#### **Adds Aspose.ThreeD.Formats.GLTFLoadOptions Class**
We have added GLTFLoadOptions class. It helps in importing glTF files into Aspose.3D API.

**Flip the V/T Texture Coordinate**

{{< highlight java >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.GLTFSaveOptions Class**
We have added GLTFSaveOptions class. It defines settings on saving a glTF file.

**Embed Dependencies Inside the Output glTF File**

{{< highlight java >}}

 // the code example creates a glTF file that has a sphere, and embed all assets into the target file

// usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders

// use opt.EmbedAssets to tells the aspose.3D to export scene and embed the dependencies inside the target file.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.EmbedAssets = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Use KHR_materials_common Extensions to Define the Materials**

{{< highlight java >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Customize the Filename of Buffer File**

{{< highlight java >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Creates a Binary glTF File using KHR_binary_glTF Extension**

{{< highlight java >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Creates a Binary glTF File using KHR_binary_glTF Extension along with Saving Options**

{{< highlight java >}}

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
#### **Adds glTF Format Entry in the Aspose.ThreeD.FileFormat Class**
We have added a GLTF and GLTF_Binary format entries for loading and saving purposes.
#### **Adds an Extension property in the Aspose.ThreeD.FileFormatType Class**
We have added an Extension property in the FileFormatType class to get the extension name of the file format.
### **Write Dependencies in the Real File System**
Using the recent version (16.11.0) or higher, developers can save all 3D scene dependencies in the real file system. Developers may define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Adds Aspose.ThreeD.Utilities.DummyFileSystem Class**
**Discard Saving the Material Files**

{{< highlight java >}}

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
#### **Adds Aspose.ThreeD.Utilities.LocalFileSystem Class**
**Save Dependencies in the Local Directory**

{{< highlight java >}}

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
#### **Adds Aspose.ThreeD.Utilities.MemoryFileSystem Class**
**Save Dependencies in the MemoryFileSystem Object**

{{< highlight java >}}

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
### **Adds FileSystem property in the Aspose.ThreeD.Formats.IOConfig Class**
We have added a FileSystem property in the IOConfig class to write dependencies.

**Adds a FileSystem property**

{{< highlight java >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
