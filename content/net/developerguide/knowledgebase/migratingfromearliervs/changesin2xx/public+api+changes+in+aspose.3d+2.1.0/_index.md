---
title : "Public API Changes in Aspose.3D 2.1.0" 
description : "" 
weight : 20082 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin2xx/public+api+changes+in+aspose.3d+2.1.0/
---

# Aspose.3D for .NET : Public API Changes in Aspose.3D 2.1.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Adds Export of Collada Files](#adds-export-of-collada-files)
*   [Adds Load and Save Options for 3D File Formats](#adds-load-and-save-options-for-3d-file-formats)
    *   [Adds Aspose.ThreeD.Formats.ColladaSaveOptions class](#adds-aspose.threed.formats.colladasaveoptions-class)
    *   [Adds Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class](#adds-aspose.threed.formats.discreet3dsloadoptions-class)
    *   [Adds Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class](#adds-aspose.threed.formats.discreet3dssaveoptions-class)
    *   [Adds Aspose.ThreeD.Formats.FBXSaveOptions Class](#adds-aspose.threed.formats.fbxsaveoptions-class)
    *   [Adds Aspose.ThreeD.Formats.ObjLoadOptions Class](#adds-aspose.threed.formats.objloadoptions-class)
    *   [Adds Aspose.ThreeD.Formats.ObjSaveOptions Class](#adds-aspose.threed.formats.objsaveoptions-class)
    *   [Adds Aspose.ThreeD.Formats.STLLoadOptions Class](#adds-aspose.threed.formats.stlloadoptions-class)
    *   [Adds Aspose.ThreeD.Formats.STLSaveOptions Class](#adds-aspose.threed.formats.stlsaveoptions-class)
    *   [Adds Aspose.ThreeD.Formats.U3DLoadOptions Class](#adds-aspose.threed.formats.u3dloadoptions-class)
    *   [Adds Aspose.ThreeD.Formats.U3DSaveOptions Class](#adds-aspose.threed.formats.u3dsaveoptions-class)
*   [Adds Methods to Aspose.ThreeD.Scene Class](#adds-methods-to-aspose.threed.scene-class)
*   [Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class](#removal-of-filldummyindexarray-property-from-aspose.threed.formats.fbxconfig-class)
*   [Detect the Type of a 3D File](#detect-the-type-of-a-3d-file)
    *   [Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class](#adds-detect,-createloadoptions-and-createsaveoptions-methods-in-the-aspose.threed.fileformat-class)
*   [Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes](#adds-excluded-property-to-aspose.threed.entity-and-aspose.threed.node-classes)
*   [Adds Aspose.ThreeD.Render.RenderState Class and Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums](#adds-aspose.threed.render.renderstate-class-and-aspose.threed.render.blendfactor/comparefunction/cullfacemode/frontface/polygonmode/stencilaction/stencilstate-enums)
*   [Adds Shader APIs](#adds-shader-apis)
    *   [Adds an abstract class Aspose.ThreeD.Render.ShaderSource and sub class Aspose.ThreeD.Render.GLSLSource](#adds-an-abstract-class-aspose.threed.render.shadersource-and-sub-class-aspose.threed.render.glslsource)
    *   [Adds Aspose.ThreeD.Render.ShaderException Class](#adds-aspose.threed.render.shaderexception-class)
    *   [Adds Aspose.ThreeD.Render.ShaderProgram Class](#adds-aspose.threed.render.shaderprogram-class)
    *   [Add Aspose.ThreeD.Render.ShaderVariable Class](#add-aspose.threed.render.shadervariable-class)
    *   [Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic](#adds-an-enum-class-aspose.threed.render.variablesemantic)
*   [Adds Buffer APIs](#adds-buffer-apis)
    *   [Adds an Interface Aspose.ThreeD.Render.IBuffer](#adds-an-interface-aspose.threed.render.ibuffer)
    *   [Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#adds-interfaces-aspose.threed.render.iindexbuffer/ivertexbuffer)
    *   [Adds an Enum Aspose.ThreeD.Render.IndexDataType](#adds-an-enum-aspose.threed.render.indexdatatype)
*   [Adds Render APIs](#adds-render-apis)
    *   [Adds an Interface Aspose.ThreeD.Render.IRenderable](#adds-an-interface-aspose.threed.render.irenderable)
    *   [Added an Enum Aspose.ThreeD.Render.DrawOperation](#added-an-enum-aspose.threed.render.drawoperation)
    *   [Adds an Enum Aspose.ThreeD.Render.RenderQueueGroupId](#adds-an-enum-aspose.threed.render.renderqueuegroupid)
    *   [Adds Aspose.ThreeD.Render.RenderResource Class](#adds-aspose.threed.render.renderresource-class)
    *   [Adds Aspose.ThreeD.Render.RenderableResource Class](#adds-aspose.threed.render.renderableresource-class)
    *   [Adds Aspose.ThreeD.Entities.ManualEntity Class](#adds-aspose.threed.entities.manualentity-class)
*   [Adds Multiple Triangulate Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#adds-multiple-triangulate-methods-in-the-aspose.threed.entities.polygonmodifier-class)
*   [Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class](#adds-createvertexbuffer,-createindexbuffer,-createtextureunit,-createrenderstate-and-createshaderprogram-methods-in-the-aspose.threed.render.renderfactory-class)
*   [Adds BindRenderState, DrawIndexed, Draw and SubmitRenderTask Methods in the Aspose.ThreeD.Render.Renderer Class](#adds-bindrenderstate,-drawindexed,-draw-and-submitrendertask-methods-in-the-aspose.threed.render.renderer-class)
*   [Adds RenderStage and Shader Properties in the Aspose.ThreeD.Render.Renderer Class](#adds-renderstage-and-shader-properties-in-the-aspose.threed.render.renderer-class)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 2.0.0 to 2.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

### Adds Export of Collada Files

Using this recent version (2.1.0), developers can export Collada 3D files. In the previous version (2.0.0), we have already added its import feature, since developers can also convert a Collada file to other supported 3D file formats.

### Adds Load and Save Options for 3D File Formats

We have added load and save options for each file format. They're refactored from the original IOConfig subclasses.

#### Adds Aspose.ThreeD.Formats.ColladaSaveOptions class

It defines settings on saving a Collada 3D file.

**C#**

{{< code lang="c#" >}}
ColladaSaveOptions opts = new ColladaSaveOptions();
// generates indented XML document
opts.Indented = true;
// the style of node transformation
opts.TransformStyle = ColladaTransformStyle.Matrix;
// configure the look up paths to allow importer to find external dependencies.
opts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class

It defines settings on loading a discreet 3DS file.

**C#**

{{< code lang="c#" >}}
Discreet3DSLoadOptions loadOpts = new Discreet3DSLoadOptions();
// sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.ApplyAnimationTransform = true;
// flip the coordinate system
loadOpts.FlipCoordinateSystem = true;
// prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.GammaCorrectedColor = true;
// configure the look up paths to allow importer to find external dependencies.
loadOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class

It defines settings on saving a discreet 3DS file.

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.FBXSaveOptions Class

It defines settings on saving an FBX file.

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.ObjLoadOptions Class

It defines settings on loading an Obj file.

**C#**

{{< code lang="c#" >}}
// initialize an object
ObjLoadOptions loadObjOpts = new ObjLoadOptions();
// import materials from external material library file
loadObjOpts.EnableMaterials = true;
// flip the coordinate system.
loadObjOpts.FlipCoordinateSystem = true;
// configure the look up paths to allow importer to find external dependencies.
loadObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.ObjSaveOptions Class

It defines settings on saving an Obj file.

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.STLLoadOptions Class

It defines settings on loading an STL file.

**C#**

{{< code lang="c#" >}}
// initialize an object
STLLoadOptions loadSTLOpts = new STLLoadOptions();
// flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.STLSaveOptions Class

It defines settings on saving an STL file.

**C#**

{{< code lang="c#" >}}
// initialize an object
STLSaveOptions saveSTLOpts = new STLSaveOptions();
// flip the coordinate system.
saveSTLOpts.FlipCoordinateSystem = true;
// configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.U3DLoadOptions Class

It defines settings on loading a U3D file.

**C#**

{{< code lang="c#" >}}
// initialize an object
U3DLoadOptions loadU3DOpts = new U3DLoadOptions();
// flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.U3DSaveOptions Class

It defines settings on saving a U3D file.

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

### Adds Methods to Aspose.ThreeD.Scene Class

We have overloaded Open and Save methods in the Scene class. Developers can pass a stream object or direct file name to import/export a 3D file using the various loading/saving options.

**C#**

{{< code lang="c#" >}}
public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);
public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);
public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);
public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);
{{< /code >}}

### Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class

This property was not being used.

**C#**

{{< code lang="c#" >}}
System.Nullable<Boolean> FillDummyIndexArray{ get;set;}
{{< /code >}}

### Detect the Type of a 3D File

The Detect method of the Aspose.ThreeD.FileFormat class can recognise the type of any supported 3D file.

**C#**

FileFormat inputFormat = FileFormat.Detect(@"C:\\ThreeD\\test06\\colors.fbx");Console.WriteLine("File Format: " + inputFormat.ToString());

#### Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class

After the recognition of a 3D file type, developers can create LoadOptions and SaveOptions objects for the further manipulation tasks.

**C#**

// allows to detect file format from file stream or filenamestatic Aspose.ThreeD.FileFormat Detect(System.IO.Stream stream, string fileName)// allows to detect file format from filenamestatic Aspose.ThreeD.FileFormat Detect(string fileName)// create default load options for this file formatAspose.ThreeD.Formats.LoadOptions CreateLoadOptions()// create default save options for this file formatAspose.ThreeD.Formats.SaveOptions CreateSaveOptions()

### Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes

It allows an entity to be removed during the export.

**C#**

bool Excluded{ get;set;}

### Adds Aspose.ThreeD.Render.RenderState Class and Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums

The render states provide parameters for the GPU to rasterize triangles into pixels.

Encapsulation of hardware render states, detail information can be found at the documentation of [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489(v=vs.85).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327(v=vs.85).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

### Adds Shader APIs

The Shader APIs define how to transform the triangles from world space into screen space and calculate the final pixel color in GPU side.

#### Adds an abstract class Aspose.ThreeD.Render.ShaderSource and sub class Aspose.ThreeD.Render.GLSLSource

The GLSLSource tells renderer, the source code is for OpenGL shading language, it can be compiled to Aspose.ThreeD.Render.ShaderProgram.

#### Adds Aspose.ThreeD.Render.ShaderException Class

The Shader related exceptions, mainly used in the shader language compiling and linking stage.

#### Adds Aspose.ThreeD.Render.ShaderProgram Class

It is the compiled shader program.

#### Add Aspose.ThreeD.Render.ShaderVariable Class

It defines the variables used in shader.

#### Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic

It is used to identify the shader variable's semantic, Aspose.3D renderer will automatically prepare shader variable values depends on the semantics.

### Adds Buffer APIs

The buffers provide definition and data of the triangles.

#### Adds an Interface Aspose.ThreeD.Render.IBuffer

It is the base interface for IIndexBuffer and IVertexBuffer.

#### Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer

They present hardware buffers for storing the geometry indices.

#### Adds an Enum Aspose.ThreeD.Render.IndexDataType

The datatype of the geometry indices.

### Adds Render APIs

#### Adds an Interface Aspose.ThreeD.Render.IRenderable

An object that supports rendering should implement this interface.

#### Added an Enum Aspose.ThreeD.Render.DrawOperation

The primitive type to draw.

#### Adds an Enum Aspose.ThreeD.Render.RenderQueueGroupId

Aspose.3D API uses render queue to manage the render workflow, this is used to submit render operation to specified render queue.

#### Adds Aspose.ThreeD.Render.RenderResource Class

Base class for bridging the Aspose.3D's model API to hardware resources, this is used by Aspose.3D internally, but exposed to unleash the full power of Aspose.3D rendering.

#### Adds Aspose.ThreeD.Render.RenderableResource Class

A Sub class of RenderResource, but concentrate on rendering.

#### Adds Aspose.ThreeD.Entities.ManualEntity Class

The user should use this class to implement their own entity that supports rendering, this class encapsulates the details of rendering operations and resource management.

### Adds Multiple Triangulate Methods in the Aspose.ThreeD.Entities.PolygonModifier Class

More overloads to simplify the usage of original function.

**C#**

public static int\[\]\[\] Triangulate(IList<\[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int\[\]> polygons);public static int\[\]\[\] Triangulate(IList<\[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32\[\] polygon);public static int\[\]\[\] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

### Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class

**C#**

public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()public Aspose.ThreeD.Render.RenderState CreateRenderState()public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

### Adds BindRenderState, DrawIndexed, Draw and SubmitRenderTask Methods in the Aspose.ThreeD.Render.Renderer Class

**C#**

public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

### Adds RenderStage and Shader Properties in the Aspose.ThreeD.Render.Renderer Class

**C#**

public RenderStage RenderStage { get; }public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

