---
title: Spécifiez 3D Options de sauvegarde du fichier dans C#
linktitle: Spécifiez les options de sauvegarde de fichier 3D
type: docs
weight: 40
url: /fr/net/specify-3d-file-save-options/
description: Il existe plusieurs surcharges de méthode Scene.Save qui acceptent un objet SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde.
---
##  **Aperçu**

Cet article explique comment vous pouvez enregistrer des fichiers 3D dans différents formats [Après les avoir chargés dans l'objet Scène](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) en utilisant C#. En chargeant et en sauvegardant, vous pouvez effectuer un nombre de conversions différentes, par ex.

- Convertir FBX en X en C#
- Convertir GLTF en OBJ en C#
- Convertir OBJ en X en C#
- Convertir STL en OBJ en C#
- Convertir RVM en 3DS en C#

##  **3D Options de sauvegarde des fichiers**
Il existe plusieurs surcharges de méthode [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui acceptent un objet SaveOptions. Cela devrait être un objet d'une classe dérivée de la classe `SaveOptions`. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde, par exemple, il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
###  **Utilisation des options de sauvegarde Collada**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Collada.

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
###  **Utilisation des options de sauvegarde Discreet3DS**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un fichier 3D dans un format Discreet 3DS.

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
###  **Utilisation des options de sauvegarde FBX**
Le code C# ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un fichier 3D au format FBX.

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

`FBXSaveOptions` expose également la propriété `EnableCompression` qui peut être utilisée pour compresser de grandes données binaires dans le fichier FBX. La valeur par défaut de cette propriété est true. L'extrait de code ci-dessous explique comment vous pouvez travailler avec cette propriété tout en enregistrant une scène.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3D document into Aspose.3D
            Scene scene = Scene.FromFile"document.fbx");

            scene.Save("UncompressedDocument.fbx", new FbxSaveOptions(FileFormat.FBX7500ASCII) { EnableCompression = false });

{{< /highlight >}}
###  **Utilisation des options Obj Save**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Obj.

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
###  **Utilisation des options de sauvegarde STL**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlSaveOptions saveSTLOpts = new StlSaveOptions();
// Flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Utilisation des options de sauvegarde U3D**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format U3D.

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
###  **Utilisation des options de sauvegarde glTF**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 



Le code C# ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format glTF.

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
###  **PrettyPrint in glTF Options de sauvegarde**
Vous pouvez également utiliser la propriété PrettyPrint de la classe GLTFSaveOptions pour une impression JSON compréhensible par l'homme. Le code ci-dessous montre comment utiliser cette fonctionnalité.

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
###  **Enregistrer les dépendances d'une scène 3D dans le système de fichiers réel**
Les développeurs peuvent avoir besoin d'enregistrer toutes les dépendances de scène 3D dans le système de fichiers réel. Ils peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet `MemoryFileSystem` ou simplement jeter les dépendances. La propriété `FileSystem` est ajoutée dans toutes les classes d'options de sauvegarde.
####  **Jeter l'enregistrement des fichiers matériels**
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
####  **Sauvegardez les dépendances dans le répertoire local**
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
####  **Sauvegardez les dépendances dans l'objet MemoryFileSystem**
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
###  **Utilisation des options de sauvegarde Google Draco (.drc)**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format DRC.

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
###  **Utilisation des options de sauvegarde RVM**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format RVM.

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
