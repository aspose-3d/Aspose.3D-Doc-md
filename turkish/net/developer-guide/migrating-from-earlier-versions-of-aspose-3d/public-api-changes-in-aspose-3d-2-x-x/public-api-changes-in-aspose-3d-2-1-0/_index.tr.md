---
title: Public API Changes Aspose.3D 2.1.0
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Contents Summary**

- [Collada Files dds dds Export](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [3D File Formats için dds dds Load ve Save ptions ptions](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Dds dds Aspose.ThreeD.Formats. ColladaSaveptions ptions sınıfı](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Dds dds Aspose.ThreeD.Formats.Discreet3DSLoadOptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats.Discreet3DSSaveOptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. Flass aveaveavelass ptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. bjbjLoadlass ptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. bjbjSavelass ptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. Slass lass ooadlass ptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. Slass aveaveavelass ptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. U3Dooadlass ptions lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Dds dds Aspose.ThreeD.Formats. U3Daveavelass ptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Dds dds Methods Aspose.ThreeD.Scene lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Removal of 0707roperty from Aspose.ThreeD.Formats. Flass onononfig lass lass](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Detect bir 3D File Type](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Dds dds Detect, CreateLoadOptions ve Createreave07ptions eethods Aspose.ThreeD. Fileiormat lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Dds dds Excluded Property Aspose.ThreeD.Entity ve Aspose.ThreeD.Node sses lasses](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Dds dds Aspose.ThreeD.Render. Rendertate tate lass lass ve Aspose.ThreeD.Render. actor lendactor actor/Compareununction/Cullulaceoode/Frontnumace/Polygongonode/StencilAction/Stenciltate tate numnums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Dds dds Shader AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Dds dds bir soyut sınıf Aspose.ThreeD.Render. Shaderourource ve alt sınıf Aspose.ThreeD.Render. GLourourourource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Dds dds Aspose.ThreeD.Render. Shaderhaxception lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Dds dds Aspose.ThreeD.Render. Shaderharogram lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Add Aspose.ThreeD.Render. Shaderariariable lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Dds dds bir Enum lass 07Aspose.ThreeD. Render. Variableariemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Dds dds ffer uffer AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Dds dds an Interface Aspose.ThreeD.Render. Iffer uffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Dds dds Interfaces Aspose.ThreeD.Render. Inndexnuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Dds dds bir Enum Aspose.ThreeD.Render. Indexnatayype](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Dds dds Render AIIs](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Dds dds an Interface Aspose.ThreeD.Render. Iderenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Abir Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Dds dds bir Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Dds dds Aspose.ThreeD.Render. Rendersource esource lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Dds dds Aspose.ThreeD.Render. Renderablesource esource lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Dds dds Aspose.ThreeD.Entities.ManualEntity lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Dds dds ultiultiple 07riangulate 07ethods Aspose.ThreeD.Entities. olyolygongonodifier lass lass](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Dds dds CreateVertexBuffer, Createnndex. uffer, Createreexturenit nit, Createreendertate tate ve Createrehaderrorogram Methods Aspose.ThreeD.Render. Rendertory actory lass lass ffer uffer](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Dds dds BindRendertate tate, DrawInderaw, Draw ve Submit07enderask ask ask ethods Aspose.ThreeD.Render.Renderer lass lass ask](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Aspose.ThreeD.Render. enenderer lass lass içinde dds dds Rendertage tage ve Shader Properties](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

This belgesi, 2.0.0 sürümünden 2.1.0 'a kadar Aspose.3D API 'teki değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Collada Files dds dds Export**
Ubu son sürümü (2.1.0) söyleyin, geliştiriciler Collada 3D dosyalarını ihraç edebilir. In önceki sürümü (2.0.0), zaten ithalat özelliğini ekledik, çünkü geliştiriciler Collada dosyasını desteklenen diğer 3D dosya formatlarına da dönüştürebilirler.
### **3D File Formats için dds dds Load ve Save ptions ptions**
We, her dosya formatı için yükleme ve kaydetme seçenekleri ekledi. They, orijinal IOfig onfig alt sınıflarından yeniden üretildi.
#### **Dds dds Aspose.ThreeD.Formats. ColladaSaveptions ptions sınıfı**
It, Collada 3D dosyasını kaydetme ayarlarını tanımlar.

**C#**

{{< highlight "csharp" >}}

 ColladaSaveOptions opts = new ColladaSaveOptions();

// generates indented XML document

opts.Indented = true;

// the style of node transformation

opts.TransformStyle = ColladaTransformStyle.Matrix;

// configure the look up paths to allow importer to find external dependencies.

opts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats.Discreet3DSLoadOptions lass lass**
It, gizli bir 3DS dosyası yüklemede ayarları tanımlar.

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

loadOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats.Discreet3DSSaveOptions lass lass**
It, gizli bir 3DS dosyasını kaydetme ayarlarını tanımlar.

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

saveOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

// set the master scale

saveOpts.MasterScale = 1;

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. Flass aveaveavelass ptions lass lass**
It, FBX dosyasını kaydetme ayarlarını tanımlar.

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

saveOpts.LookupPaths = new List< string > (new string[]{ @"c:\temp\" });

// generates a video object for texture.

saveOpts.VideoForTexture = true;

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. bjbjLoadlass ptions lass lass**
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

loadObjOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. bjbjSavelass ptions lass**
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

saveObjOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

// serialize W component in model's vertex position

saveObjOpts.SerializeW = true;

// generate comments for each section

saveObjOpts.Verbose = true;

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. Slass lass ooadlass ptions lass lass**
It STL dosyası yüklemede ayarları tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. Slass aveaveavelass ptions lass lass**
It, STL dosyasını kaydetme ayarlarını tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. U3Dooadlass ptions lass lass**
It U3D dosyası yüklemede ayarları tanımlar.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats. U3Daveavelass ptions lass**
It, U3D dosyasını kaydetme ayarlarını tanımlar.

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

saveU3DOptions.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

// compress the mesh data

saveU3DOptions.MeshCompression = true;

{{< /highlight >}}
### **Dds dds Methods Aspose.ThreeD.Scene lass lass**
We, cene cene sınıfında aşırı yüklü Open ve Save yöntemlerine sahiptir. Developers, çeşitli yükleme/kaydetme seçeneklerini kullanarak bir 3D dosyasını içe aktarmak/ihraç etmek için bir akış nesnesi veya doğrudan dosya adını geçebilir.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Removal of 0707roperty from Aspose.ThreeD.Formats. Flass onononfig lass lass**
Tonun mülkü kullanılmadı.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Detect bir 3D File Type**
To Aspose.ThreeD. File. ormat sınıfı, desteklenen herhangi bir 3D dosyasının türünü tanıyabilir.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Dds dds Detect, CreateLoadOptions ve Createreave07ptions eethods Aspose.ThreeD. Fileiormat lass lass**
A3D dosya türünün tanınmasını sağlayan geliştiriciler, daha fazla manipülasyon görevi için Load. ptions ve aveave. ptions nesneleri oluşturabilirler.

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
### **Dds dds Excluded Property Aspose.ThreeD.Entity ve Aspose.ThreeD.Node sses lasses**
It, ihracat sırasında bir varlığın kaldırılmasını sağlar.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Dds dds Aspose.ThreeD.Render. Rendertate tate lass lass ve Aspose.ThreeD.Render. actor lendactor actor/Compareununction/Cullulaceoode/Frontnumace/Polygongonode/StencilAction/Stenciltate tate numnums**
To, üçgenleri piksellere dönüştürmek için GPU için parametreler sağlar.

{{% alert color="primary" %}} 

Donanım capsudurumlarının kapsüllenmesi, detay bilgileri belgelerinde bulunabilir[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) ve[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Dds dds Shader AIIs**
The Shader AIIs, üçgenleri dünya alanından ekran alanına nasıl dönüştüreceğini ve GPU side 'daki son piksel rengini nasıl hesaplayacağını tanımlıyor.
#### **Dds dds bir soyut sınıf Aspose.ThreeD.Render. Shaderourource ve alt sınıf Aspose.ThreeD.Render. GLourourourource**
The GLrenourourource, kaynak kodu OpenGL gölgeleme dili içindir, Aspose.ThreeD.Render. ShaderProgram'a derlenebilir.
#### **Dds dds Aspose.ThreeD.Render. Shaderhaxception lass lass**
Shader he shader hader ile ilgili istisnalar, esas olarak gölgelendirici dilinde derleme ve bağlama aşamasında kullanılır.
#### **Dds dds Aspose.ThreeD.Render. Shaderharogram lass lass**
It derlenmiş gölgelendirici programıdır.
#### **Add Aspose.ThreeD.Render. Shaderariariable lass lass**
It gölgelendiricide kullanılan değişkenleri tanımlar.
#### **Dds dds bir Enum lass 07Aspose.ThreeD. Render. Variableariemantic**
Shader t, gölgelendirici değişkeninin anlamlılığını tanımlamak için kullanılır, Aspose.3D renderer otomatik olarak gölgelendirici değişken değerlerini semantiklere göre hazırlayacaktır.
### **Dds dds ffer uffer AIIs**
Buffo tamponlar üçgenlerin tanımını ve verilerini sağlar.
#### **Dds dds an Interface Aspose.ThreeD.Render. Iffer uffer**
It, IIndex. uffer ve IVertex. uffer için temel arabirimdir.
#### **Dds dds Interfaces Aspose.ThreeD.Render. Inndexnuffer/IVertexBuffer**
Geometry hey geometri endekslerini saklamak için mevcut donanım tamponları.
#### **Dds dds bir Enum Aspose.ThreeD.Render. Indexnatayype**
Geometry o geometri endeksleri datatype.
### **Dds dds Render AIIs**
#### **Dds dds an Interface Aspose.ThreeD.Render. Iderenderable**
Rendering n görüntülemeyi destekleyen nesne bu arayüzü uygulamalıdır.
#### **Abir Enum Aspose.ThreeD.Render.DrawOperation**
To İlkel tip çizmek için.
#### **Dds dds bir Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API, render iş akışını yönetmek için render kuyruğunu kullanır, bu, belirtilen render kuyruğuna işlem yapmak için kullanılır.
#### **Dds dds Aspose.ThreeD.Render. Rendersource esource lass lass**
Aspose.3D'in API modelini donanım kaynaklarına köprülemek için Base sınıfı, bu Aspose.3D dahili olarak kullanılır, ancak Aspose.3D renginin tam gücünü açığa çıkarır.
#### **Dds dds Aspose.ThreeD.Render. Renderablesource esource lass lass**
Rendersource esource'ın A ub ub sınıfı, ancak render üzerine yoğunlaşın.
#### **Dds dds Aspose.ThreeD.Entities.ManualEntity lass lass**
Tkullanıcı, bu sınıfı, render işlemini destekleyen kendi varlıklarını uygulamak için kullanmalı, bu sınıf işlem işlemlerinin ve kaynak yönetiminin ayrıntılarını kapsüllemektedir.
### **Dds dds ultiultiple 07riangulate 07ethods Aspose.ThreeD.Entities. olyolygongonodifier lass lass**
Orijinal fonksiyonun kullanımını kolaylaştırmak için aşırı yükler.

**C#**

{{< highlight "csharp" >}}

 public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[]polygon);

public static int[][]Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Dds dds CreateVertexBuffer, Createnndex. uffer, Createreexturenit nit, Createreendertate tate ve Createrehaderrorogram Methods Aspose.ThreeD.Render. Rendertory actory lass lass ffer uffer**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Dds dds BindRendertate tate, DrawInderaw, Draw ve Submit07enderask ask ask ethods Aspose.ThreeD.Render.Renderer lass lass ask**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Aspose.ThreeD.Render. enenderer lass lass içinde dds dds Rendertage tage ve Shader Properties**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
