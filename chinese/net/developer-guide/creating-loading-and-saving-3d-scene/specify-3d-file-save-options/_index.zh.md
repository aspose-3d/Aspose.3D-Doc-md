---
title: 在 C# 中指定 3D 文件保存选项
linktitle: 指定 3D 文件保存选项
type: docs
weight: 40
url: /zh/net/specify-3d-file-save-options/
description: 有几个场景。保存方法重载接受一个SaveOptions对象。每种保存格式都有一个相应的类，该类保存该保存格式的保存选项。
---
##  **概述**

本文介绍如何使用 C# 将 3D 文件保存为不同的格式 [将它们加载到场景对象后](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)。通过加载和保存，您可以执行不同的转换数量。

- 在 C# 中将 FBX 转换为X
- 在 C# 中将 GLTF 转换为 OBJ
- 在 C# 中将 OBJ 转换为X
- 在 C# 中将 STL 转换为 OBJ
- 在 C# 中将 RVM 转换为 3DS

##  **3D 文件保存选项**
有几个接受SaveOptions对象的 [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) 方法重载。这应该是从 `SaveOptions` 类派生的类的对象。每种保存格式都有一个对应的类，该类包含该保存格式的保存选项，例如，对于 `FileFormat.Collada` 保存格式，有 `ColladaSaveOptions`。
###  **使用 Collada 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 Collada 格式之前设置保存选项。

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
###  **使用 Discreet3DS 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为谨慎的 3DS 格式之前设置保存选项。

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
###  **使用 FBX 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 FBX 格式之前设置保存选项。

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

`FBXSaveOptions` 还公开了 `EnableCompression` 属性，该属性可用于压缩 FBX 文件中的大型二进制数据。此属性的默认值为true。下面的代码片段解释了如何在保存场景时使用此属性。



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3D document into Aspose.3D
            Scene scene = Scene.FromFile"document.fbx");

            scene.Save("UncompressedDocument.fbx", new FbxSaveOptions(FileFormat.FBX7500ASCII) { EnableCompression = false });

{{< /highlight >}}
###  **使用Obj保存选项**
下面的代码显示了如何在将 3D 文件保存为Obj格式之前设置保存选项。

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
###  **使用 STL 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 STL 格式之前设置保存选项。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlSaveOptions saveSTLOpts = new StlSaveOptions();
// Flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **使用 U3D 保存选项**
下面的 C# 代码显示了如何在将文档保存为 U3D 格式之前设置保存选项。

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
###  **使用 glTF 保存选项**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 



下面的 C# 代码显示了如何在将文档保存为 glTF 格式之前设置保存选项。

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
###  **glTF 保存选项中的PrettyPrint**
您还可以使用GLTFSaveOptions类的PrettyPrint属性进行人类可理解的JSON打印。下面的代码显示了如何使用此功能。

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
###  **在真实文件系统中保存 3D 场景的依赖项**
开发人员可能需要将所有 3D 场景依赖项保存在真实文件系统中。它们可以定义本地目录的路径，保存在 `MemoryFileSystem` 对象中或简单地丢弃依赖项。`FileSystem` 属性被添加到所有保存选项类中。
####  **放弃保存材料文件**
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
####  **在本地目录中保存依赖项**
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
####  **在MemoryFileSystem对象中保存依赖关系**
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
###  **使用 Google Draco (.drc) 保存选项**
下面的 C# 代码显示了如何在将 3D 模型保存为 DRC 格式之前设置保存选项。

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
###  **使用 RVM 保存选项**
下面的 C# 代码显示了如何在将 3D 模型保存为 RVM 格式之前设置保存选项。

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
