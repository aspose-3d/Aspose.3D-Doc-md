---
title: Публичные изменения API в Aspose.3D 16.11.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Содержание Резюме**

- [Добавляет метод AddEntity в класс Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Импорт и экспорт файлов glTF](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Adds Aspose.ThreeD.Formats.GLTFLoadOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.GLTFSaveOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Adds glTF Format Entry in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Adds an Extension property in the Aspose.ThreeD.FileFormatType Class](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Записывайте зависимости в реальной файловой системе](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Adds Aspose.ThreeD.Utilities.DummyFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Adds Aspose.ThreeD.Utilities.LocalFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Adds Aspose.ThreeD.Utilities.MemoryFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Добавляет свойство FileSystem в класс Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 16.9.0 до 16.11.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Добавляет метод AddEntity в класс Aspose.ThreeD.Node**
Срезанный способ добавления объекта к узлу.

**Добавить Entity в узел**

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
###  **Импорт и экспорт файлов glTF**
Используя последнюю версию (16.11.0) или выше, разработчики могут импортировать и экспортировать файлы glTF в/из других поддерживаемых файлов 3D.
####  **Добавляет Aspose.ThreeD. Форматы. Класс GLTFLoadOptions**
Мы добавили класс GLTFLoadOptions. Он помогает импортировать glTF файлов в Aspose.3D API.

**Переверните координату текстуры V/T**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **Добавляет Aspose.ThreeD. Форматы. Класс GLTFSaveOptions**
Мы добавили класс GLTFSaveOptions. Он определяет настройки при сохранении файла glTF.

**Встраивание зависимостей внутри выходного файла glTF**

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

**Используйте KHR_materials_common Extensions, чтобы определить материалы**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Настроить имя файла буферного файла**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Создает двоичный файл glTF с помощью расширения KHR_binary_glTF**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Создает двоичный файл glTF с помощью расширения KHR_binary_glTF вместе с параметрам сохранения**

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
####  **Добавляет запись формата glTF в класс Aspose.ThreeD.FileFormat**
Мы добавили записи формата GLTF и GLTF_Binary для загрузки и сохранения.
####  **Добавление свойства Extension в класс Aspose.ThreeD.FileFormatType**
Мы добавили свойство Extension в классе FileFormatType, чтобы получить имя расширения формата файла.
###  **Записывайте зависимости в реальной файловой системе**
Используя последнюю версию (16.11.0) или выше, разработчики могут сохранить все зависимости сцены 3D в реальной файловой системе. Разработчики могут определить путь к локальной директории, сохранить в объекте MemoryFileSystem или просто отказаться от зависимостей. Свойство FileSystem добавляется во все классы параметров сохранения.
####  **Добавляет Aspose.ThreeD. Утилиты. DummyFileSystem Класс**
**Откажите сохранение файлов материала**

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
####  **Добавляет класс Aspose.ThreeD.Utilities.LocalFileSystem**
**Сохранить зависимости в локальном каталоге**

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
####  **Добавляет Aspose.ThreeD. Утилиты. Класс MemoryFileSystem**
**Сохранение зависимостей в объекте MemoryFileSystem**

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
###  **Добавляет свойство FileSystem в класс Aspose.ThreeD.Formats.IOConfig**
Для записи зависимостей мы добавили свойство FileSystem в класс IOConfig.

**Добавляет свойство FileSystem**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
