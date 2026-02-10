---
title: Especificar las opciones de guardado de archivos 3D en C#
linktitle: Especificar las opciones de guardado de archivos 3D
type: docs
weight: 40
url: /es/net/specify-3d-file-save-options/
description: Hay varias sobrecargas del método Scene.Save que aceptan un objeto SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado.
---
##  **Descripción general**

Este artículo explica cómo puede guardar archivos 3D en diferentes formatos [Después de cargarlos en objeto Escena](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) usando C#. Al cargar y guardar, puede realizar varias conversiones diferentes, p.

- Convertir FBX a X en C#
- Convierte GLTF a OBJ en C#
- Convertir OBJ a X en C#
- Convierte STL a OBJ en C#
- Convierte RVM a 3DS en C#

##  **3D Opciones para guardar archivos**
Hay varias sobrecargas de método [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) que aceptan un objeto SaveOptions. Debe ser un objeto de una clase derivada de la clase `SaveOptions`. Cada formato de guardado tiene una clase correspondiente que contiene las opciones de guardado para ese formato de guardado, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de guardado Collada**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en el formato Collada.

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
###  **Uso de las opciones de guardado Discreet3DS**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Discreet 3DS.

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
###  **Uso de las opciones de guardado FBX**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato FBX.

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

`FBXSaveOptions` también expone la propiedad `EnableCompression` que se puede usar para comprimir datos binarios grandes en el archivo FBX. El valor predeterminado de esta propiedad es true. A continuación, el fragmento de código explica cómo puede trabajar con esta propiedad mientras guarda una escena.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3D document into Aspose.3D
            Scene scene = Scene.FromFile"document.fbx");

            scene.Save("UncompressedDocument.fbx", new FbxSaveOptions(FileFormat.FBX7500ASCII) { EnableCompression = false });

{{< /highlight >}}
###  **Uso de las opciones de Obj Save**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Obj.

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
###  **Uso de las opciones de guardado STL**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en el formato STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlSaveOptions saveSTLOpts = new StlSaveOptions();
// Flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Uso de las opciones de guardado U3D**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un documento en formato U3D.

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
###  **Uso de las opciones de guardado glTF**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 



El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un documento en formato glTF.

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
###  **PrettyPrint en glTF Guardar opciones**
También puede utilizar la propiedad PrettyPrint de la clase GLTFSaveOptions para la impresión JSON comprensible para el ser humano. El siguiente código muestra cómo usar esta funcionalidad.

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
###  **Guardar dependencias de una escena 3D en el sistema de archivos real**
Los desarrolladores pueden requerir guardar todas las dependencias de escena 3D en el sistema de archivos real. Pueden definir la ruta de un directorio local, guardar en el objeto `MemoryFileSystem` o simplemente descartar dependencias. La propiedad `FileSystem` se agrega en las clases de opción all save.
####  **Descarte guardar los archivos de material**
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
####  **Guardar dependencias en el directorio local**
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
####  **Guardar dependencias en el objeto MemoryFileSystem**
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
###  **Uso de las opciones de guardado Google Draco (.drc)**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato DRC.

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
###  **Uso de las opciones de guardado RVM**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato RVM.

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
