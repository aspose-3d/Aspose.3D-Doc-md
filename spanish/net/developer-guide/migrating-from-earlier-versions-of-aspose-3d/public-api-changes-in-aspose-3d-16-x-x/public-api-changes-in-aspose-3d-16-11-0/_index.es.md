---
title: Público API Cambios en Aspose.3D 16.11.0
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Resumen de contenidos**

- [Agrega el método AddEntity en la clase Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Importación y exportación de archivos glTF](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
[Agrega la clase Aspose.ThreeD.Formats. GlTFLoadOptions](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats. GSTFSaveOptions](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
[Agrega una entrada de formato glTF en la clase Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
[Agrega una propiedad Extension en la clase Aspose.ThreeD.FileFormatType](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Escribir dependencias en el sistema de archivos reales](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
[Agrega la clase Aspose.ThreeD.Utilities.DummyFileSystem](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
[Agrega la clase Aspose.ThreeD.Utilities.LocalFileSystem](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
[Agrega la clase Aspose.ThreeD.Utilities.MemoryFileSystem](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Agrega la propiedad FileSystem en la clase Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.9.0 to 16.11.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Agrega el método AddEntity en la clase Aspose.ThreeD.Node**
Una vía de acceso directo para agregar una entidad a un nodo.

**Agregar una entidad a un nodo**

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
###  **Importación y exportación de archivos glTF**
Utilizando la versión reciente (16.11.0) o superior, los desarrolladores pueden importar y exportar archivos glTF a/desde otros archivos 3D compatibles.
####  **Agrega la clase Aspose.ThreeD.Formats. GlTFLoadOptions**
Hemos añadido la clase de GlTFLoadOptions. Ayuda a importar archivos glTF en Aspose.3D API.

**Voltear la coordenadas de textura V/T**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **Agrega la clase Aspose.ThreeD.Formats. GSTFSaveOptions**
Hemos añadido la clase de GlTFSaveOptions. Define la configuración para guardar un archivo glTF.

**Incrustar dependencias dentro del archivo glTF de salida**

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

**Utilice las extensiones KHR_materials_common para definir los materiales**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Personalizar el nombre de archivo de búfer**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Crea un archivo glTF binario usando la extensión KHR_binary_glTF**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Crea un archivo glTF binario usando la extensión KHR_binary_glTF junto con las opciones de guardado**

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
####  **Agrega una entrada de formato glTF en la clase Aspose.ThreeD.FileFormat**
Hemos añadido entradas en formato GLTF y GLTF_Binary para cargar y guardar.
####  **Agrega una propiedad Extension en la clase Aspose.ThreeD.FileFormatType**
Hemos agregado una propiedad Extension en la clase FileFormatType para obtener el nombre de la extensión del formato de archivo.
###  **Escribir dependencias en el sistema de archivos reales**
Con la versión reciente (16.11.0) o superior, los desarrolladores pueden guardar todas las dependencias de escena 3D en el sistema de archivos real. Los desarrolladores pueden definir la ruta de un directorio local, guardar en el objeto MemoryFileSystem o simplemente descartar dependencias. La propiedad FileSystem se agrega en las clases de opción all save.
####  **Agrega la clase Aspose.ThreeD.Utilities.DummyFileSystem**
**Descarte guardar los archivos de material**

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
####  **Agrega la clase Aspose.ThreeD.Utilities.LocalFileSystem**
**Guardar dependencias en el directorio local**

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
####  **Agrega la clase Aspose.ThreeD.Utilities.MemoryFileSystem**
**Guardar dependencias en el objeto MemoryFileSystem**

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
###  **Agrega la propiedad FileSystem en la clase Aspose.ThreeD.Formats.IOConfig**
Hemos agregado una propiedad FileSystem en la clase IOConfig para escribir dependencias.

**Agrega una propiedad FileSystem**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
