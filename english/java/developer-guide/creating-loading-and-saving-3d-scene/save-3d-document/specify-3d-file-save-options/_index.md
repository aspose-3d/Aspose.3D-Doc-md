---
title: Specify 3D File Save Options
type: docs
weight: 10
url: /java/specify-3d-file-save-options/
description: There are several Scene.save method overloads that accept a SaveOptions instance.
---

## **3D File Save Options**
There are several Scene.save method overloads that accept a SaveOptions instance. This should be an instance of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example there is ColladaSaveOptions for the FileFormat.COLLADA save format.
### **Use of Collada Save Options**
The code below shows how to set save options before saving a 3D file in Collada format.

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
### **Use of Discreet3DS Save Options**
The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

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
### **Use of the FBX Save Options**
The code below shows how to set save options before saving a 3D file to an FBX format.

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
### **Use of OBJ Save Options**
The code below shows how to set save options before saving a 3D file to an Obj format.

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
### **Use of STL Save Options**
The code below shows how to set save options before saving a 3D file to STL format.

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
### **Use of the U3D Save Options**
The code below shows how to set save options before saving a document to U3D format.

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
### **Use of the glTF Save Options**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 



The code below shows how to set save options before saving a document to glTF format.

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
### **PrettyPrint in glTF Save Options**
You can also use setPrettyPrint method of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

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
### **Save Dependencies of a 3D Scene in the Real File System**
Developers may require to save all dependencies of 3D scene in the real file system. They can define the path of a local directory, save in the `MemoryFileSystem` object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Discard Saving the Material Files**
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
#### **Save Dependencies in the Local Directory**
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
#### **Save Dependencies in the MemoryFileSystem Instance**
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
### **Use of the Google Draco (.DRC) Save Options**
The code below shows how to set save options before saving a 3D model to DRC format.

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
### **Use of RVM Save Options**
The code below shows how to set save options before saving a 3D model to RVM format.

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
