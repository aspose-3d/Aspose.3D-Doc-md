---
title: Spécifiez les options de sauvegarde de fichier 3D
type: docs
weight: 10
url: /fr/java/specify-3d-file-save-options/
description: Il existe plusieurs surcharges de méthode Scene.save qui acceptent une instance SaveOptions.
---
##  **3D Options de sauvegarde des fichiers**
Il existe plusieurs surcharges de méthode Scene.save qui acceptent une instance SaveOptions. Il doit s'agir d'une instance d'une classe dérivée de la classe SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient les options de sauvegarde pour ce format de sauvegarde, par exemple il existe ColladaSaveOptions pour le format de sauvegarde FileFormat.COLLADA.
###  **Utilisation des options de sauvegarde Collada**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Collada.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
ColladaSaveOptions saveColladaopts = new ColladaSaveOptions();
// Generates indented XML document
saveColladaopts.setIndented(true);
// The style of node transformation
saveColladaopts.setTransformStyle(ColladaTransformStyle.MATRIX);
// Configure the lookup paths to allow importer to find external dependencies.
saveColladaopts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde Discreet3DS**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D dans un format Discreet 3DS.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
Discreet3DSSaveOptions saveOpts = new Discreet3DSSaveOptions();
// The start base for generating new name for duplicated names.
saveOpts.setDuplicatedNameCounterBase(2);
// The format of the duplicated counter.
saveOpts.setDuplicatedNameCounterFormat("NameFormat");
// The separator between object's name and the duplicated counter.
saveOpts.setDuplicatedNameSeparator("Separator");
// Allows to export cameras
saveOpts.setExportCamera(true);
// Allows to export light
saveOpts.setExportLight(true);
// Flip the coordinate system
saveOpts.setFlipCoordinateSystem(true);
// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
saveOpts.setGammaCorrectedColor(true);
// Use high-precise color which each color channel will use 32bit float.
saveOpts.setHighPreciseColor(true);
// Configure the look up paths to allow importer to find external dependencies.
saveOpts.getLookupPaths().add(MyDir);
// Set the master scale
saveOpts.setMasterScale(1);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde FBX**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D dans un format FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
FBXSaveOptions saveOpts = new FBXSaveOptions(FileFormat.ASE);
// Generates the legacy material properties.
saveOpts.setExportLegacyMaterialProperties(true);
// Fold repeated curve data using FBX's animation reference count
saveOpts.setFoldRepeatedCurveData(true);
// Always generates material mapping information for geometries if the attached node contains materials.
saveOpts.setGenerateVertexElementMaterial(true);
// Configure the look up paths to allow importer to find external dependencies.
saveOpts.getLookupPaths().add(MyDir);
// Generates a video object for texture.
saveOpts.setVideoForTexture(true);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde OBJ**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Obj.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
ObjSaveOptions saveObjOpts = new ObjSaveOptions();
// Import materials from external material library file
saveObjOpts.setEnableMaterials(true);
// Flip the coordinate system.
saveObjOpts.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
saveObjOpts.getLookupPaths().add(MyDir);
// Serialize W component in model's vertex position
saveObjOpts.setSerializeW(true);
// Generate comments for each section
saveObjOpts.setVerbose(true);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde STL**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format STL.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
STLSaveOptions saveSTLOpts = new STLSaveOptions();
// Flip the coordinate system.
saveSTLOpts.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde U3D**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format U3D.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
U3DSaveOptions saveU3DOptions = new U3DSaveOptions();
// Export normal data.
saveU3DOptions.setExportNormals(true);
// Export the texture coordinates.
saveU3DOptions.setExportTextureCoordinates(true);
// Export the vertex diffuse color.
saveU3DOptions.setExportVertexDiffuse(true);
// Export vertex specular color
saveU3DOptions.setExportVertexSpecular(true);
// Flip the coordinate system.
saveU3DOptions.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
saveU3DOptions.getLookupPaths().add(MyDir);
// Compress the mesh data
saveU3DOptions.setMeshCompression(true);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde glTF**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 



Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format glTF.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.getRootNode().createChildNode("sphere", new Sphere());
// Set glTF saving options. The code example embeds all assets into the target file usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders
// Use opt.EmbedAssets to tells the Aspose.3D API to export scene and embed the dependencies inside the target file.
GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);
opt.setEmbedAssets(true);
// Use KHR_materials_common extension to define the material, thus no GLSL files are generated.
opt.setUseCommonMaterials(true);
// Customize the name of the buffer file which defines model
opt.setBufferFile("mybuf.bin");
// Save glTF file
scene.save(MyDir + "glTFSaveOptions_out.gltf", opt);
 
// Save a binary glTF file using KHR_binary_glTF extension
scene.save(MyDir + "glTFSaveOptions_out.glb", FileFormat.GLTF__BINARY);
 
// Developers may use saving options to create a binary glTF file using KHR_binary_glTF extension
GLTFSaveOptions opts = new GLTFSaveOptions(FileContentType.BINARY);
scene.save(MyDir + "Test_out.glb", opts);
{{< /highlight >}}
###  **PrettyPrint in glTF Options de sauvegarde**
Vous pouvez également utiliser la méthode setPrettyPrint de la classe GLTFSaveOptions pour une impression JSON compréhensible par l'homme. Le code ci-dessous montre comment utiliser cette fonctionnalité.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize 3D scene
Scene scene = new Scene(new Sphere());
// Initialize GLTFSaveOptions
GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);
// opt.prettyPrint = true; //Old code
// The JSON content of GLTF file is indented for human reading, default value is false
// Use setter to change this configuration.
opt.setPrettyPrint(true);
// Save 3D Scene
scene.save(RunExamples.getDataDir() + "prettyPrintInGltfSaveOption.gltf", opt);

{{< /highlight >}}
###  **Enregistrer les dépendances d'une scène 3D dans le système de fichiers réel**
Les développeurs peuvent avoir besoin d'enregistrer toutes les dépendances de la scène 3D dans le système de fichiers réel. Ils peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet `MemoryFileSystem` ou simplement jeter les dépendances. La propriété FileSystem est ajoutée dans toutes les classes d'option de sauvegarde.
####  **Jeter l'enregistrement des fichiers matériels**
{{< highlight "java" >}}
// The code example uses the DummyFileSystem, so the material files are not created.
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.getRootNode().createChildNode("sphere", new Sphere()).setMaterial(new PhongMaterial());
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
opt.setFileSystem(new DummyFileSystem());
// Save 3D scene
scene.save(MyDir + "DiscardSavingMaterial_out.obj", opt);
{{< /highlight >}}
####  **Sauvegardez les dépendances dans le répertoire local**
{{< highlight "java" >}}
// The code example uses the LocalFileSystem class to save dependencies to the local directory.
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.getRootNode().createChildNode("sphere", new Sphere()).setMaterial(new PhongMaterial());
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
opt.setFileSystem(new LocalFileSystem(MyDir));
// Save 3D scene
scene.save(MyDir + "SavingDependenciesInLocalDirectory_out.obj", opt);
{{< /highlight >}}
####  **Sauvegardez les dépendances dans l'instance MemoryFileSystem**
{{< highlight "java" >}}
// The code example uses the MemoryFileSystem to intercepts the dependencies writing.
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.getRootNode().createChildNode("sphere", new Sphere()).setMaterial(new PhongMaterial());
// Set saving options
ObjSaveOptions opt = new ObjSaveOptions();
MemoryFileSystem mfs = new MemoryFileSystem();
opt.setFileSystem(mfs);
// Save 3D scene
scene.save(MyDir + "SavingDependenciesInMemoryFileSystem_out.obj", opt);
// Get the test.mtl file content
byte[] mtl = mfs.getFileContent(MyDir + "SavingDependenciesInMemoryFileSystem_out.mtl");
Files.write(Paths.get(MyDir, "Material.mtl"), mtl);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde Google Draco (.DRC)**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un modèle 3D au format DRC.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene object
Scene scene = new Scene();
// Create a child node
scene.getRootNode().createChildNode("sphere", new Sphere());
// Initialize .DRC saving options.
DracoSaveOptions opts = new DracoSaveOptions();
// Quantization bits for position
opts.setPositionBits(14);
// Quantization bits for texture coordinate
opts.setTextureCoordinateBits(8);
// Quantization bits for vertex color
opts.setColorBits(10);
// Quantization bits for normal vectors
opts.setNormalBits(7);
// Set compression level
opts.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
// Save Google Draco (.drc) file
scene.save(MyDir + "DRCSaveOptions_out.drc", opts);
{{< /highlight >}}
###  **Utilisation des options de sauvegarde RVM**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un modèle 3D au format RVM.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
String dataDir = RunExamples.getDataDir();
Scene scene = new Scene();
Node node = scene.getRootNode().createChildNode("Box", new Box());
node.setProperty("rvm:Refno", "=3462123");
node.setProperty("rvm:Description", "This is the description of the box");
//The RVM attribute's prefix is rvm:, all properties that starts with rvm: will be exported to .att file(the prefix will be removed)
RvmSaveOptions opt = new RvmSaveOptions();
opt.setAttributePrefix( "rvm:");
opt.setExportAttributes(true);
scene.save(dataDir + "test.rvm", opt);

{{< /highlight >}}
