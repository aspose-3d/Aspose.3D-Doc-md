---
title: Kamu API Aspose içinde değişir. 3D 2.1.0
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Contents Summary**

- [Collada dosyalarının ihracatını ekler](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Yükleme ve kaydetme seçeneklerini 3D dosya biçimleri için ekler](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
-[Aspose ekler. threed. formats. colladasaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
-[Aspose ekler. threed. formats. discreet3dslotions tions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
-[Aspose ekler. threed. formats. discreet3dssaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
-[Aspose ekler. threed. formats. fbxsaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
-[Aspose ekler. threed. formats. objobdodosınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
-[Aspose ekler. threed. formats. objsaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
-[Aspose ekler. threed. formats. stlloadodosınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
-[Aspose ekler. threed. formats. stlsaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
-[Aspose ekler. threed. formats. u3dloadoclass sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
-[Aspose ekler. threed. formats. u3dsaveoptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Adds Methods to Aspose.ThreeD.Scene Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [3D dosyasının türünü tespit et](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
-[Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Aspose ekler. threed. ren. renderstate sınıfı ve Aspose. threed. blen. blendfactor/comparefunction/cullfacemode/frontface/polygonmode/stencilaction/stencilstate enums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Dds dds Shader AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
-[Soyut bir sınıf Aspose ekler. threed. render. shsource kaynak ve alt sınıf Aspose. threed. gl. glslsource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
-[Aspose ekler. threed. render. shaderexception sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
-[Adds Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
-[Add Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
-[Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Dds dds ffer uffer AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
-[Adds an Interface Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
-[Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
-[Bir enum Aspose ekler. threed. render. indexdatatype](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Dds dds Render AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
-[Adds an Interface Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
-[Bir enum Aspose eklendi. threed. render. drawoperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
-[Bir enum Aspose ekler. threed. render. renderqueuegroupid](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
-[Adds Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
-[Aspose ekler. threed. render. renderableresource sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
-[Adds Aspose.ThreeD.Entities.ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Aspose. threed. entities. polygonmodifier sınıfında çoklu üçgenleme yöntemleri ekler](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Bindrenderstate, drawindexed, draw ve submitrendertask yöntemlerini Aspose. threed. render. renderer sınıfında ekler](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Aspose. threed. render. renderer sınıfında renderstage ve gölgelendirici özellikleri ekler](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Bu belge, Aspose.3D API sürüm 2.0.0 'den 2.1.0 'a kadar olan değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. Sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'daki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
###  **Collada dosyalarının ihracatını ekler**
Using this recent version (2.1.0), developers can export Collada 3D files. In the previous version (2.0.0), we have already added its import feature, since developers can also convert a Collada file to other supported 3D file formats.
###  **Yükleme ve kaydetme seçeneklerini 3D dosya biçimleri için ekler**
We, her dosya formatı için yükleme ve kaydetme seçenekleri ekledi. They, orijinal IOfig onfig alt sınıflarından yeniden üretildi.
####  **Aspose ekler. threed. formats. colladasaveoptions sınıfı**
Collada 3D dosyasını kaydetme ayarlarını tanımlar.

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
####  **Aspose ekler. threed. formats. discreet3dslotions tions sınıfı**
Gizli bir 3DS dosyası yüklemede ayarları tanımlar.

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
####  **Aspose ekler. threed. formats. discreet3dssaveoptions sınıfı**
Gizli bir 3DS dosyasını kaydetme ayarlarını tanımlar.

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
####  **Aspose ekler. threed. formats. fbxsaveoptions sınıfı**
FBX dosyasını kaydetme ayarlarını tanımlar.

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
####  **Aspose ekler. threed. formats. objobdodosınıfı**
It, bir Obj dosyası yüklemede ayarları tanımlar.

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
####  **Aspose ekler. threed. formats. objsaveoptions sınıfı**
It, bir Obj dosyasını kaydetme ayarlarını tanımlar.

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
####  **Aspose ekler. threed. formats. stlloadodosınıfı**
STL dosyasını yüklemede ayarları tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aspose ekler. threed. formats. stlsaveoptions sınıfı**
STL dosyasını kaydetme ayarlarını tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aspose ekler. threed. formats. u3dloadoclass sınıfı**
U3D dosyasını yüklemede ayarları tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aspose ekler. threed. formats. u3dsaveoptions sınıfı**
U3D dosyasını kaydetme ayarlarını tanımlar.

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
###  **Adds Methods to Aspose.ThreeD.Scene Class**
We have overloaded Open and Save methods in the Scene class. Developers can pass a stream object or direct file name to import/export a 3D file using the various loading/saving options.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **Removal of FillDummyIndexArray Property from Aspose.ThreeD.Formats.FBXConfig Class**
Tonun mülkü kullanılmadı.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **3D dosyasının türünü tespit et**
The Detect method of the Aspose.ThreeD.FileFormat class can recognise the type of any supported 3D file.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class**
3D dosya türünün tanınmasından sonra, geliştiriciler daha fazla manipülasyon görevi için ptions do. ve saveoptions nesneleri oluşturabilirler.

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
###  **Adds Excluded Property to Aspose.ThreeD.Entity and Aspose.ThreeD.Node Classes**
It, ihracat sırasında bir varlığın kaldırılmasını sağlar.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **Aspose ekler. threed. ren. renderstate sınıfı ve Aspose. threed. blen. blendfactor/comparefunction/cullfacemode/frontface/polygonmode/stencilaction/stencilstate enums**
To, üçgenleri piksellere dönüştürmek için GPU için parametreler sağlar.

{{% alert color="primary" %}} 

Donanım render durumlarının kapsüllenmesi, detay bilgileri [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [Direct11 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) ve [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo) belgelerinde bulunabilir.

{{% /alert %}} 
###  **Dds dds Shader AIIs**
The Shader AIIs, üçgenleri dünya alanından ekran alanına nasıl dönüştüreceğini ve GPU side 'daki son piksel rengini nasıl hesaplayacağını tanımlıyor.
####  **Soyut bir sınıf Aspose ekler. threed. render. shsource kaynak ve alt sınıf Aspose. threed. gl. glslsource**
The GLSLSource tells renderer, the source code is for OpenGL shading language, it can be compiled to Aspose.ThreeD.Render.ShaderProgram.
####  **Aspose ekler. threed. render. shaderexception sınıfı**
Shader he shader hader ile ilgili istisnalar, esas olarak gölgelendirici dilinde derleme ve bağlama aşamasında kullanılır.
####  **Adds Aspose.ThreeD.Render.ShaderProgram Class**
It derlenmiş gölgelendirici programıdır.
####  **Add Aspose.ThreeD.Render.ShaderVariable Class**
It gölgelendiricide kullanılan değişkenleri tanımlar.
####  **Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic**
Gölgelendirici değişkeninin semantik, Aspose.3D renderer otomatik olarak gölgelendirici değişken değerlerini semantiklere göre hazırlayacaktır.
###  **Dds dds ffer uffer AIIs**
Buffo tamponlar üçgenlerin tanımını ve verilerini sağlar.
####  **Adds an Interface Aspose.ThreeD.Render.IBuffer**
It, IIndex. uffer ve IVertex. uffer için temel arabirimdir.
####  **Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
Geometry hey geometri endekslerini saklamak için mevcut donanım tamponları.
####  **Bir enum Aspose ekler. threed. render. indexdatatype**
Geometry o geometri endeksleri datatype.
###  **Dds dds Render AIIs**
####  **Adds an Interface Aspose.ThreeD.Render.IRenderable**
Rendering n görüntülemeyi destekleyen nesne bu arayüzü uygulamalıdır.
####  **Bir enum Aspose eklendi. threed. render. drawoperation**
To İlkel tip çizmek için.
####  **Bir enum Aspose ekler. threed. render. renderqueuegroupid**
Aspose.3D API render iş akışını yönetmek için render kuyruğunu kullanır, bu, belirtilen render kuyruğuna işlem yapmak için kullanılır.
####  **Adds Aspose.ThreeD.Render.RenderResource Class**
Base class for bridging the Aspose.3D's model API to hardware resources, this is used by Aspose.3D internally, but exposed to unleash the full power of Aspose.3D rendering.
####  **Aspose ekler. threed. render. renderableresource sınıfı**
Rendersource esource'ın A ub ub sınıfı, ancak render üzerine yoğunlaşın.
####  **Adds Aspose.ThreeD.Entities.ManualEntity Class**
Tkullanıcı, bu sınıfı, render işlemini destekleyen kendi varlıklarını uygulamak için kullanmalı, bu sınıf işlem işlemlerinin ve kaynak yönetiminin ayrıntılarını kapsüllemektedir.
###  **Aspose. threed. entities. polygonmodifier sınıfında çoklu üçgenleme yöntemleri ekler**
Orijinal fonksiyonun kullanımını kolaylaştırmak için aşırı yükler.

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **Adds CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState and CreateShaderProgram Methods in the Aspose.ThreeD.Render.RenderFactory Class**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **Bindrenderstate, drawindexed, draw ve submitrendertask yöntemlerini Aspose. threed. render. renderer sınıfında ekler**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **Aspose. threed. render. renderer sınıfında renderstage ve gölgelendirici özellikleri ekler**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
