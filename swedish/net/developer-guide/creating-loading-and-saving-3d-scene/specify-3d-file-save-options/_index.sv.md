---
title: Ange 3D Filspararalternativ i C#
linktitle: Ange 3D Filspararalternativ
type: docs
weight: 40
url: /sv/net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
##  **Översikt**

Den här artikeln förklarar hur du kan spara 3D filer i olika format [Efter att ha laddat dem i Sceneobjekt](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) med C#. Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till X i C#
- Konvertera GLTF till OBJ i C#
- Konvertera OBJ till X i C#
- Konvertera STL till OBJ i C#
- Konvertera RVM till 3DS i C#

##  **3D Filspararalternativ**
Det finns flera överbelastningar med [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett SparaOptions-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `SaveOptions`. Varje format spara har en motsvarande klass som innehåller sparalternativ för det spara formatet, till exempel, det finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Användning av Collada Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i Collada-format.

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
###  **Användning av Discreet3DS Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i ett diskret 3DS-format.

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
###  **Användning av FBX Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska anges innan en 3D-fil sparas till ett FBX-format.

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

`FBXSaveOptions` exponerar också `EnableCompression` egenskap som kan användas för att komprimera större binärdata i FBX-filen. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3D document into Aspose.3D
            Scene scene = Scene.FromFile"document.fbx");

            scene.Save("UncompressedDocument.fbx", new FbxSaveOptions(FileFormat.FBX7500ASCII) { EnableCompression = false });

{{< /highlight >}}
###  **Användning av Obj Spara alternativen**
Koden nedan visar hur sparalternativ ska anges innan en 3D fil sparas till ett Obj-format.

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
###  **Användning av STL Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i STL-format.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlSaveOptions saveSTLOpts = new StlSaveOptions();
// Flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Användning av U3D Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska anges innan ett dokument sparas i U3D-format.

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
###  **Användning av glTF Spara inställningarna**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



C#-koden nedan visar hur sparalternativ ska anges innan ett dokument sparas i glTF-format.

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
###  **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

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
###  **Spara beroenden för en 3D i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D-scener i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i `MemoryFileSystem`- objektet eller helt enkelt förkasta beroenden. Egenskapen `FileSystem` läggs till i alla spara alternativklasser.
####  **Kasta sparande av materialfiler**
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
####  **Spara beroende i lokalkatalog**
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
####  **Spara beroende i MemoryFileSystem- objekt**
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
###  **Användning av Google Draco (.drc) Spara inställningar**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till DRC-format.

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
###  **Användning av RVM Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till RVM-format.

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
