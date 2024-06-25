---
title: Aspose.3D 2.1.0中的公共 API 更改
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-3d-2-1-0/
---
**内容摘要**

- [添加 Collada 个文件的导出](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [为 3D 文件格式添加加载和保存选项](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
-[添加 Aspose.ThreeD.Formats.ColladaSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
-[添加 Aspose.ThreeD.Formats.Discreet3dsladoptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
-[添加 Aspose.ThreeD.Formats.Discreet3DSSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
-[添加 Aspose.ThreeD.Formats.FBXSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
-[添加 Aspose.ThreeD.Formats.Objlodopadoptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
-[添加 Aspose.ThreeD.Formats.ObjSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
-[添加 Aspose.ThreeD.Formats.STLLoadOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
-[添加 Aspose.ThreeD.Formats.STLSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
-[添加 Aspose.ThreeD.Formats.U3DLoadOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
-[添加 Aspose.ThreeD.Formats.U3DSaveOptions类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [将方法添加到 Aspose.ThreeD.Scene类](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [从 Aspose.ThreeD.Formats.FBXConfig类中删除FillDummyIndexArray属性](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [检测 3D 文件的类型](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
-[在 Aspose.ThreeD.FileFormat类中添加Detect、CreateLoadOptions和CreateSaveOptions方法](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [将排除的属性添加到 Aspose.ThreeD.Entity和 Aspose.ThreeD.Node类](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [添加 Aspose.ThreeD.Render.RenderState类和 Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState枚举](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [添加着色器api](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
-[添加抽象类 Aspose.ThreeD.Render.ShaderSource和子类 Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
-[添加 Aspose.ThreeD.Render.ShaderException类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
-[添加 Aspose.ThreeD.Render.ShaderProgram类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
-[添加 Aspose.ThreeD.Render.ShaderVariable类](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
-[添加枚举类 Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [添加缓冲区api](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
-[添加接口 Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
-[添加接口 Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
-[添加枚举 Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [添加渲染api](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
-[添加接口 Aspose.ThreeD.Render.Irendable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
-[添加了一个枚举 Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
-[添加枚举 Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
-[添加 Aspose.ThreeD.Render.RenderResource类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
-[添加 Aspose.ThreeD.Render.RenderableResource类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
-[添加 Aspose.ThreeD.Entities.ManualEntity类](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [在 Aspose.ThreeD.Entities.PolygonModifier类中添加多个三角化方法](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [在 Aspose.ThreeD.Render.RenderFactory类中添加CreateVertexBuffer、CreateIndexBuffer、CreateTextureUnit、CreateRenderState和CreateShaderProgram方法](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [在 Aspose.ThreeD.Render.Renderer类中添加BindRenderState、DrawIndexed、Draw和SubmitRenderTask方法](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [在 Aspose.ThreeD.Render.Renderer类中添加RenderStage和Shader属性](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从2.0.0版到2.1.0版的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **添加 Collada 个文件的导出**
使用此最新版本 (2.1.0)，开发人员可以导出 Collada 3D 文件。在之前的版本 (2.0.0) 中，我们已经添加了它的导入功能，因为开发人员还可以将 Collada 文件转换为其他支持的 3D 文件格式。
###  **为 3D 文件格式添加加载和保存选项**
我们为每种文件格式添加了加载和保存选项。它们是从原始的IOConfig子类重构的。
####  **添加 Aspose.ThreeD.Formats.ColladaSaveOptions类**
它定义了保存 Collada 3D 文件的设置。

**C#**

{{< highlight "csharp" >}}

 ColladaSaveOptions opts = new ColladaSaveOptions();

// generates indented XML document

opts.Indented = true;

// the style of node transformation

opts.TransformStyle = ColladaTransformStyle.Matrix;

// configure the look up paths to allow importer to find external dependencies.

opts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.Discreet3dsladoptions类**
它定义加载离散 3DS 文件的设置。

**C#**

{{< highlight "csharp" >}}

 Discreet3DSLoadOptions loadOpts = new Discreet3DSLoadOptions();

// sets weather to use the transformation defined in the first frame of animation track.

loadOpts.ApplyAnimationTransform = true;

// flip the coordinate system

loadOpts.FlipCoordinateSystem = true;

// prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.

loadOpts.GammaCorrectedColor = true;

// configure the look up paths to allow importer to find external dependencies.

loadOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.Discreet3DSSaveOptions类**
它定义了保存谨慎的 3DS 文件的设置。

**C#**

{{< highlight "csharp" >}}

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
####  **添加 Aspose.ThreeD.Formats.FBXSaveOptions类**
它定义了保存 FBX 文件的设置。

**C#**

{{< highlight "csharp" >}}

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
####  **添加 Aspose.ThreeD.Formats.Objlodopadoptions类**
它定义加载Obj文件时的设置。

**C#**

{{< highlight "csharp" >}}

 // initialize an object

ObjLoadOptions loadObjOpts = new ObjLoadOptions();

// import materials from external material library file

loadObjOpts.EnableMaterials = true;

// flip the coordinate system.

loadObjOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.ObjSaveOptions类**
它定义了保存Obj文件的设置。

**C#**

{{< highlight "csharp" >}}

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
####  **添加 Aspose.ThreeD.Formats.STLLoadOptions类**
它定义加载 STL 文件的设置。

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.STLSaveOptions类**
它定义了保存 STL 文件的设置。

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.U3DLoadOptions类**
它定义加载 U3D 文件时的设置。

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.U3DSaveOptions类**
它定义了保存 U3D 文件的设置。

**C#**

{{< highlight "csharp" >}}

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
###  **将方法添加到 Aspose.ThreeD.Scene类**
我们在Scene类中重载了Open和Save方法。开发人员可以使用各种加载/保存选项传递流对象或直接文件名以导入/导出 3D 文件。

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **从 Aspose.ThreeD.Formats.FBXConfig类中删除FillDummyIndexArray属性**
该属性没有被使用。

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **检测 3D 文件的类型**
Aspose.ThreeD.FileFormat类的Detect方法可以识别任何受支持的 3D 文件的类型。

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **在 Aspose.ThreeD.FileFormat类中添加Detect、CreateLoadOptions和CreateSaveOptions方法**
识别 3D 文件类型后，开发人员可以为进一步的操作任务创建LoadOptions和SaveOptions对象。

**C#**

{{< highlight "csharp" >}}

 // allows to detect file format from file stream or filename

static Aspose.ThreeD.FileFormat Detect(System.IO.Stream stream, string fileName)

// allows to detect file format from filename

static Aspose.ThreeD.FileFormat Detect(string fileName)

// create default load options for this file format

Aspose.ThreeD.Formats.LoadOptions CreateLoadOptions()

// create default save options for this file format

Aspose.ThreeD.Formats.SaveOptions CreateSaveOptions()

{{< /highlight >}}
###  **将排除的属性添加到 Aspose.ThreeD.Entity和 Aspose.ThreeD.Node类**
它允许在导出过程中删除实体。

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **添加 Aspose.ThreeD.Render.RenderState类和 Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState枚举**
渲染状态为GPU提供了将三角形栅格化为像素的参数。

{{% alert color="primary" %}} 

硬件呈现状态的封装，详细信息可以在 [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml) 、 [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx) 、 [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) 和 [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo) 的文档中找到

{{% /alert %}} 
###  **添加着色器api**
Shader api定义了如何将三角形从世界空间转换到屏幕空间，并在GPU端计算最终的像素颜色。
####  **添加抽象类 Aspose.ThreeD.Render.ShaderSource和子类 Aspose.ThreeD.Render.GLSLSource**
GLSLSource告诉渲染器，源代码是OpenGL着色语言，它可以编译为 Aspose.ThreeD.Render.ShaderProgram。
####  **添加 Aspose.ThreeD.Render.ShaderException类**
着色器相关的异常，主要用于着色器语言编译和链接阶段。
####  **添加 Aspose.ThreeD.Render.ShaderProgram类**
它是编译后的着色器程序。
####  **添加 Aspose.ThreeD.Render.ShaderVariable类**
它定义了着色器中使用的变量。
####  **添加枚举类 Aspose.ThreeD.Render.VariableSemantic**
它用于标识着色器变量的语义 Aspose。3D 渲染器将根据语义自动准备着色器变量值。
###  **添加缓冲区api**
缓冲区提供三角形的定义和数据。
####  **添加接口 Aspose.ThreeD.Render.IBuffer**
它是IIndexBuffer和IVertexBuffer的基本接口。
####  **添加接口 Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
它们提供了用于存储几何索引的硬件缓冲区。
####  **添加枚举 Aspose.ThreeD.Render.IndexDataType**
几何索引的数据类型。
###  **添加渲染api**
####  **添加接口 Aspose.ThreeD.Render.Irendable**
支持渲染的对象应该实现这个接口。
####  **添加了一个枚举 Aspose.ThreeD.Render.DrawOperation**
要绘制的原始类型。
####  **添加枚举 Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose。3D API 使用渲染队列管理渲染工作流，用于将渲染操作提交到指定的渲染队列。
####  **添加 Aspose.ThreeD.Render.RenderResource类**
用于将 Aspose.3D 的模型 API 桥接到硬件资源的基类，它由 Aspose.3D 在内部使用，但公开以释放 Aspose.3D 渲染的全部功能。
####  **添加 Aspose.ThreeD.Render.RenderableResource类**
RenderResource的子类，但专注于渲染。
####  **添加 Aspose.ThreeD.Entities.ManualEntity类**
用户应该使用这个类来实现自己支持渲染的实体，这个类封装了渲染操作和资源管理的细节。
###  **在 Aspose.ThreeD.Entities.PolygonModifier类中添加多个三角化方法**
更多重载，以简化原始函数的使用。

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **在 Aspose.ThreeD.Render.RenderFactory类中添加CreateVertexBuffer、CreateIndexBuffer、CreateTextureUnit、CreateRenderState和CreateShaderProgram方法**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **在 Aspose.ThreeD.Render.Renderer类中添加BindRenderState、DrawIndexed、Draw和SubmitRenderTask方法**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **在 Aspose.ThreeD.Render.Renderer类中添加RenderStage和Shader属性**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
