---
title: Укажите 3D Параметры сохранения файла в C#
linktitle: Укажите параметры сохранения файла 3D
type: docs
weight: 40
url: /ru/net/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.Save, которые принимают объект SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения.
---
##  **Обзор**

В этой статье объясняется, как сохранить файлы 3D в разных форматах [После загрузки их в объекте Scene](https://docs.aspose.com/3d/net/specify-3d-file-load-options/), используя C#. Загрузив и сохранив, вы можете выполнить ряд различных преобразований, например

- Конвертировать FBX в X в C#
- Конвертировать GLTF в OBJ в C#
- Конвертировать OBJ в X в C#
- Конвертировать STL в OBJ в C#
- Конвертировать RVM в 3DS в C#

##  **3D Параметры сохранения файла**
Существует несколько перегрузок метода [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene), которые принимают объект SaveOptions. Это должен быть объект класса, производного от класса `SaveOptions`. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
###  **Использование параметров сохранения Collada**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Collada.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
ColladaSaveOptions saveColladaopts = new ColladaSaveOptions();
// Generates indented XML document
saveColladaopts.Indented = true;
// The style of node transformation
saveColladaopts.TransformStyle = ColladaTransformStyle.Matrix;
// Configure the lookup paths to allow importer to find external dependencies.
saveColladaopts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Использование параметров сохранения Discreet3DS**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Discreet 3DS.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
Discreet3dsSaveOptions saveOpts = new Discreet3dsSaveOptions();
// The start base for generating new name for duplicated names.
saveOpts.DuplicatedNameCounterBase = 2;
// The format of the duplicated counter.
saveOpts.DuplicatedNameCounterFormat = "NameFormat";
// The separator between object's name and the duplicated counter.
saveOpts.DuplicatedNameSeparator = "Separator";
// Allows to export cameras
saveOpts.ExportCamera = true;
// Allows to export light
saveOpts.ExportLight = true;
// Flip the coordinate system
saveOpts.FlipCoordinateSystem = true;
// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
saveOpts.GammaCorrectedColor = true;
// Use high-precise color which each color channel will use 32bit float.
saveOpts.HighPreciseColor = true;
// Configure the look up paths to allow importer to find external dependencies.
saveOpts.LookupPaths = new List<string>(new string[] { "textures" });
// Set the master scale
saveOpts.MasterScale = 1;

{{< /highlight >}}
###  **Использование параметров сохранения FBX**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
FbxSaveOptions saveOpts = new FbxSaveOptions(FileFormat.FBX7500ASCII);
// Generates the legacy material properties.
saveOpts.ExportLegacyMaterialProperties = true;
// Fold repeated curve data using FBX's animation reference count
saveOpts.FoldRepeatedCurveData = true;
// Always generates material mapping information for geometries if the attached node contains materials.
saveOpts.GenerateVertexElementMaterial = true;
// Configure the look up paths to allow importer to find external dependencies.
saveOpts.LookupPaths = new List<string>(new string[] { "textures" });
// Generates a video object for texture.
saveOpts.VideoForTexture = true;

{{< /highlight >}}

`FBXSaveOptions` также предоставляет свойство `EnableCompression`, которое можно использовать для сжатия больших двоичных данных в файле FBX. Значение этого свойства по умолчанию-true. Ниже фрагмент кода объясняет, как вы можете работать с этим свойством при сохранении сцены.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3D document into Aspose.3D
            Scene scene = Scene.FromFile"document.fbx");

            scene.Save("UncompressedDocument.fbx", new FbxSaveOptions(FileFormat.FBX7500ASCII) { EnableCompression = false });

{{< /highlight >}}
###  **Использование опций сохранения Obj**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Obj.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
ObjSaveOptions saveObjOpts = new ObjSaveOptions();
// Import materials from external material library file
saveObjOpts.EnableMaterials = true;
// Flip the coordinate system.
saveObjOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveObjOpts.LookupPaths = new List<string>(new string[] { "textures" });
// Serialize W component in model's vertex position
saveObjOpts.SerializeW = true;
// Generate comments for each section
saveObjOpts.Verbose = true;

{{< /highlight >}}
###  **Использование параметров сохранения STL**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlSaveOptions saveSTLOpts = new StlSaveOptions();
// Flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Использование параметров сохранения U3D**
Код C# ниже показывает, как установить параметры сохранения перед сохранением документа в формате U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dSaveOptions saveU3DOptions = new U3dSaveOptions();
// Export normal data.
saveU3DOptions.ExportNormals = true;
// Export the texture coordinates.
saveU3DOptions.ExportTextureCoordinates = true;
// Export the vertex diffuse color.
saveU3DOptions.ExportVertexDiffuse = true;
// Export vertex specular color
saveU3DOptions.ExportVertexSpecular = true;
// Flip the coordinate system.
saveU3DOptions.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveU3DOptions.LookupPaths = new List<string>(new string[] { "textures/" });
// Compress the mesh data
saveU3DOptions.MeshCompression = true;

{{< /highlight >}}
###  **Использование параметров сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



Код C# ниже показывает, как установить параметры сохранения перед сохранением документа в формате glTF.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.RootNode.CreateChildNode("sphere", new Sphere());
// Set glTF saving options. The code example embeds all assets into the target file usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders
// Use opt.EmbedAssets to tells the Aspose.3D API to export scene and embed the dependencies inside the target file.
GltfSaveOptions opt = new GltfSaveOptions(FileContentType.ASCII);
opt.EmbedAssets = true;
// Use KHR_materials_common extension to define the material, thus no GLSL files are generated.
opt.UseCommonMaterials = true;
// Customize the name of the buffer file which defines model
opt.BufferFile = "mybuf.bin";
// Save GlTF file
scene.Save("glTFSaveOptions_out.gltf", opt);

// Save a binary glTF file using KHR_binary_glTF extension
scene.Save("glTFSaveOptions_out.glb");

// Developers may use saving options to create a binary glTF file using KHR_binary_glTF extension
GltfSaveOptions opts = new GltfSaveOptions(FileContentType.Binary);
scene.Save("Test_out.glb", opts);

{{< /highlight >}}
###  **PrettyPrint в glTF Параметры сохранения**
Вы также можете использовать свойство PrettyPrint класса GLTFSaveOptions для понятной для человека печати JSON. Код ниже показывает, как использовать эту функциональность.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize 3D scene
Scene scene = new Scene(new Sphere());
// Initialize GltfSaveOptions
GltfSaveOptions opt = new GltfSaveOptions(FileFormat.GLTF2);
// The JSON content of GLTF file is indented for human reading, default value is false
opt.PrettyPrint = true;
// Save 3D Scene
scene.Save("prettyPrintInGltfSaveOption.gltf", opt);

{{< /highlight >}}
###  **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчикам может потребоваться сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определить путь к локальной директории, сохранить в объекте `MemoryFileSystem` или просто отказаться от зависимостей. Свойство `FileSystem` добавляется во все классы опций сохранения.
####  **Откажите сохранение файлов материала**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The code example uses the DummyFileSystem, so the material files are not created.
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
opt.FileSystem = new DummyFileSystem();
// Save 3D scene
scene.Save("DiscardSavingMaterial_out.obj", opt);

{{< /highlight >}}
####  **Сохранить зависимости в локальном каталоге**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The code example uses the LocalFileSystem class to save dependencies to the local directory.
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
opt.FileSystem = new LocalFileSystem("local_dir/");
// Save 3D scene
scene.Save"SavingDependenciesInLocalDirectory_out.obj", opt);

{{< /highlight >}}
####  **Сохранение зависимостей в объекте MemoryFileSystem**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The code example uses the MemoryFileSystem to intercepts the dependencies writing.
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
MemoryFileSystem mfs = new MemoryFileSystem();
opt.FileSystem = mfs;
// Save 3D scene
scene.Save("SavingDependenciesInMemoryFileSystem_out.obj", opt);
// Get the test.mtl file content
byte[] mtl = mfs.GetFileContent("SavingDependenciesInMemoryFileSystem_out.mtl");
File.WriteAllBytes("Material.mtl", mtl);

{{< /highlight >}}
###  **Использование параметров сохранения Google Draco (.drc)**
Код C# ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате DRC.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.RootNode.CreateChildNode("sphere", new Sphere());
// Initialize .DRC saving options. 
DracoSaveOptions opts = new DracoSaveOptions();
// Quantization bits for position
opts.PositionBits = 14;
// Quantization bits for texture coordinate
opts.TextureCoordinateBits = 8;
// Quantization bits for vertex color
opts.ColorBits = 10;
// Quantization bits for normal vectors
opts.NormalBits = 7;
// Set compression level
opts.CompressionLevel = DracoCompressionLevel.Optimal;

// Save Google Draco (.drc) file
scene.Save("DRCSaveOptions_out.drc", opts);

{{< /highlight >}}
###  **Использование параметров сохранения RVM**
Код C# ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате RVM.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = new Scene();
var node = scene.RootNode.CreateChildNode("Box", new Box());
node.SetProperty("rvm:Refno", "=3462123");
node.SetProperty("rvm:Description", "This is the description of the box");
//The RVM attribute's prefix is rvm:, all properties that starts with rvm: will be exported to .att file(the prefix will be removed)
var opt = new RvmSaveOptions() { AttributePrefix = "rvm:", ExportAttributes = true };
scene.Save( "test.rvm", opt);

{{< /highlight >}}
