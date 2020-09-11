---
title: Public API Changes in Aspose.3D 2.1.0
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-3d-2-1-0/
---

**Contents Summary**

- [Adds Export of Collada Files](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Adds Load and Save Options for 3D File Formats](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Adds Aspose.ThreeD.Formats.ColladaSaveOptions class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Adds Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Adds Aspose.ThreeD.Formats.FBXSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Adds Aspose.ThreeD.Formats.ObjLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.ObjSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Adds Aspose.ThreeD.Formats.STLLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.STLSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Adds Aspose.ThreeD.Formats.U3DLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Adds Aspose.ThreeD.Formats.U3DSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Adds Methods to Aspose.ThreeD.Scene Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Detect the Type of a 3D File](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Adds Aspose.ThreeD.Render.RenderState Class and Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Adds Shader APIs](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Adds an abstract class Aspose.ThreeD.Render.ShaderSource and sub class Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Adds Aspose.ThreeD.Render.ShaderException Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Adds Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Add Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Adds Buffer APIs](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Adds an Interface Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Adds an Enum Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Adds Render APIs](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Adds an Interface Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Added an Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Adds an Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Adds Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Adds Aspose.ThreeD.Render.RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Adds Aspose.ThreeD.Entities.ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Adds Multiple Triangulate Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Adds BindRenderState, DrawIndexed, Draw and SubmitRenderTask Methods in the Aspose.ThreeD.Render.Renderer Class](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Adds RenderStage and Shader Properties in the Aspose.ThreeD.Render.Renderer Class](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 2.0.0 to 2.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Adds Export of Collada Files**
Using this recent version (2.1.0), developers can export Collada 3D files. In the previous version (2.0.0), we have already added its import feature, since developers can also convert a Collada file to other supported 3D file formats.
### **Adds Load and Save Options for 3D File Formats**
We have added load and save options for each file format. They're refactored from the original IOConfig sub-classes.
#### **Adds Aspose.ThreeD.Formats.ColladaSaveOptions class**
It defines settings on saving a Collada 3D file.

**C#**

{{< highlight csharp >}}

 ColladaSaveOptions opts = new ColladaSaveOptions();

// generates indented XML document

opts.Indented = true;

// the style of node transformation

opts.TransformStyle = ColladaTransformStyle.Matrix;

// configure the look up paths to allow importer to find external dependencies.

opts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class**
It defines settings on loading a discreet 3DS file.

**C#**

{{< highlight csharp >}}

 Discreet3DSLoadOptions loadOpts = new Discreet3DSLoadOptions();

// sets wheather to use the transformation defined in the first frame of animation track.

loadOpts.ApplyAnimationTransform = true;

// flip the coordinate system

loadOpts.FlipCoordinateSystem = true;

// prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.

loadOpts.GammaCorrectedColor = true;

// configure the look up paths to allow importer to find external dependencies.

loadOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class**
It defines settings on saving a discreet 3DS file.

**C#**

{{< highlight csharp >}}

 // initialize an object

Discreet3DSSaveOptions saveOpts = new Discreet3DSSaveOptions();

// the start base for generating new name for duplicated names.

saveOpts.DuplicatedNameCounterBase = 2;

// the format of the duplicated counter.

saveOpts.DuplicatedNameCounterFormat = "NameFormat";

// the separator between object's name and the duplicated counter.

saveOpts.DuplicatedNameSeparator = "Separator";

// allows to export cameras

saveOpts.ExportCamera = true;

// allows to export light

saveOpts.ExportLight = true;

// flip the coordinate system

saveOpts.FlipCoordinateSystem = true;

// prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.

saveOpts.GammaCorrectedColor = true;

// use high-precise color which each color channel will use 32bit float.

saveOpts.HighPreciseColor = true;

// configure the look up paths to allow importer to find external dependencies.

saveOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

// set the master scale

saveOpts.MasterScale = 1;

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.FBXSaveOptions Class**
It defines settings on saving an FBX file.

**C#**

{{< highlight csharp >}}

 // initialize an object

FBXSaveOptions saveOpts = new FBXSaveOptions(FileFormat.FBX7500ASCII);

// generates the legacy material properties.

saveOpts.ExportLegacyMaterialProperties = true;

// fold repeated curve data using FBX's animation reference count

saveOpts.FoldRepeatedCurveData = true;

// always generates material mapping information for geometries if the attached node contains materials.

saveOpts.GenerateVertexElementMaterial = true;

// configure the look up paths to allow importer to find external dependencies.

saveOpts.LookupPaths = new List< string > (new string[] { @"c:\temp\" });

// generates a video object for texture.

saveOpts.VideoForTexture = true;

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.ObjLoadOptions Class**
It defines settings on loading an Obj file.

**C#**

{{< highlight csharp >}}

 // initialize an object

ObjLoadOptions loadObjOpts = new ObjLoadOptions();

// import materials from external material library file

loadObjOpts.EnableMaterials = true;

// flip the coordinate system.

loadObjOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.ObjSaveOptions Class**
It defines settings on saving an Obj file.

**C#**

{{< highlight csharp >}}

 // initialize an object

ObjSaveOptions saveObjOpts = new ObjSaveOptions();

// import materials from external material library file

saveObjOpts.EnableMaterials = true;

// flip the coordinate system.

saveObjOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

// serialize W component in model's vertex position

saveObjOpts.SerializeW = true;

// generate comments for each section

saveObjOpts.Verbose = true;

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.STLLoadOptions Class**
It defines settings on loading an STL file.

**C#**

{{< highlight csharp >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.STLSaveOptions Class**
It defines settings on saving an STL file.

**C#**

{{< highlight csharp >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.U3DLoadOptions Class**
It defines settings on loading a U3D file.

**C#**

{{< highlight csharp >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.U3DSaveOptions Class**
It defines settings on saving a U3D file.

**C#**

{{< highlight csharp >}}

 // initialize an object

U3DSaveOptions saveU3DOptions = new U3DSaveOptions();

// export normal data.

saveU3DOptions.ExportNormals = true;

// export the texture coordinates.

saveU3DOptions.ExportTextureCoordinates = true;

// export the vertex diffuse color.

saveU3DOptions.ExportVertexDiffuse = true;

// export vertex specular color

saveU3DOptions.ExportVertexSpecular = true;

// flip the coordinate system.

saveU3DOptions.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveU3DOptions.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

// compress the mesh data

saveU3DOptions.MeshCompression = true;

{{< /highlight >}}
### **Adds Methods to Aspose.ThreeD.Scene Class**
We have overloaded Open and Save methods in the Scene class. Developers can pass a stream object or direct file name to import/export a 3D file using the various loading/saving options.

**C#**

{{< highlight csharp >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class**
This property was not being used.

**C#**

{{< highlight csharp >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Detect the Type of a 3D File**
The Detect method of the Aspose.ThreeD.FileFormat class can recognise the type of any supported 3D file.

**C#**

{{< highlight csharp >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class**
After the recognition of a 3D file type, developers can create LoadOptions and SaveOptions objects for the further manipulation tasks.

**C#**

{{< highlight csharp >}}

 // allows to detect file format from file stream or filename

static Aspose.ThreeD.FileFormat Detect(System.IO.Stream stream, string fileName)

// allows to detect file format from filename

static Aspose.ThreeD.FileFormat Detect(string fileName)

// create default load options for this file format

Aspose.ThreeD.Formats.LoadOptions CreateLoadOptions()

// create default save options for this file format

Aspose.ThreeD.Formats.SaveOptions CreateSaveOptions()

{{< /highlight >}}
### **Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes**
It allows an entity to be removed during the export.

**C#**

{{< highlight csharp >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Adds Aspose.ThreeD.Render.RenderState Class and Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums**
The render states provide parameters for the GPU to rasterize triangles into pixels.

{{% alert color="primary" %}} 

Encapsulation of hardware render states, detail information can be found at the documentation of [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Adds Shader APIs**
The Shader APIs define how to transform the triangles from world space into screen space and calculate the final pixel color in GPU side.
#### **Adds an abstract class Aspose.ThreeD.Render.ShaderSource and sub class Aspose.ThreeD.Render.GLSLSource**
The GLSLSource tells renderer, the source code is for OpenGL shading language, it can be compiled to Aspose.ThreeD.Render.ShaderProgram.
#### **Adds Aspose.ThreeD.Render.ShaderException Class**
The Shader related exceptions, mainly used in the shader language compiling and linking stage.
#### **Adds Aspose.ThreeD.Render.ShaderProgram Class**
It is the compiled shader program.
#### **Add Aspose.ThreeD.Render.ShaderVariable Class**
It defines the variables used in shader.
#### **Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic**
It is used to identify the shader variable's semantic, Aspose.3D renderer will automatically prepare shader variable values depends on the semantics.
### **Adds Buffer APIs**
The buffers provide definition and data of the triangles.
#### **Adds an Interface Aspose.ThreeD.Render.IBuffer**
It is the base interface for IIndexBuffer and IVertexBuffer.
#### **Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
They present hardware buffers for storing the geometry indices.
#### **Adds an Enum Aspose.ThreeD.Render.IndexDataType**
The datatype of the geometry indices.
### **Adds Render APIs**
#### **Adds an Interface Aspose.ThreeD.Render.IRenderable**
An object that supports rendering should implement this interface.
#### **Added an Enum Aspose.ThreeD.Render.DrawOperation**
The primitive type to draw.
#### **Adds an Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API uses render queue to manage the render workflow, this is used to submit render operation to specified render queue.
#### **Adds Aspose.ThreeD.Render.RenderResource Class**
Base class for bridging the Aspose.3D's model API to hardware resources, this is used by Aspose.3D internally, but exposed to unleash the full power of Aspose.3D rendering.
#### **Adds Aspose.ThreeD.Render.RenderableResource Class**
A Sub class of RenderResource, but concentrate on rendering.
#### **Adds Aspose.ThreeD.Entities.ManualEntity Class**
The user should use this class to implement their own entity that supports rendering, this class encapsulates the details of rendering operations and resource management.
### **Adds Multiple Triangulate Methods in the Aspose.ThreeD.Entities.PolygonModifier Class**
More overloads to simplify the usage of original function.

**C#**

{{< highlight csharp >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class**
**C#**

{{< highlight csharp >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Adds BindRenderState, DrawIndexed, Draw and SubmitRenderTask Methods in the Aspose.ThreeD.Render.Renderer Class**
**C#**

{{< highlight csharp >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Adds RenderStage and Shader Properties in the Aspose.ThreeD.Render.Renderer Class**
**C#**

{{< highlight csharp >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
