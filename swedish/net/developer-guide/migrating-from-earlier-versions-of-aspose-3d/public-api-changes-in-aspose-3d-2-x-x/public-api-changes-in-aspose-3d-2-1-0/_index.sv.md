---
title: Offentlig API Förändringar Aspose.3D 2,1,0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Innehåll**

- [Lägger till export av Collada filer](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Lägger till ladda och spara alternativ för 3D Filformat](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Lägger till Aspose.ThreeD. Format.ColladaSaveOptions klass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Lägger till Aspose.ThreeD. Format.Discreet3DSLoadOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Lägger till Aspose.ThreeD.Formats.Discreet3DSSaveOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.FBXSaveOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.ObjLoadOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.STLLoadOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.STLSaveOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.U3DLoadOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Lägger till Aspose.ThreeD. Format.U3DSaveOptions ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Lägger till metoder till Aspose.ThreeD.Scenklass](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Avlägsnande av FillDummyIndexArray egendom från Aspose.ThreeD.Formats.FBXConfig klass](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Detektera typ av en 3D- fil](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Lägger till detektera, CreateLoadOptions och CreateSaveOptions metoder i Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Lägger exkluderade egendom till Aspose.ThreeD.Enhet och Aspose.ThreeD.Node Klasser](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Lägger till Aspose.ThreeD. Render. RenderState Class och Aspose.ThreeD. Render. BlådFactor/ Jämförelse/CullFaceMode/FrontFace/PolygonMode / Stencils](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Lägger till Shader- API:](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Lägger till en abstrakt klass Aspose.ThreeD. Render. SkådareKälla och underklass Aspose.ThreeD. Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Lägger till Aspose.ThreeD.Render.ShaderException klass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Lägger till Aspose.ThreeD.Render.ShaderProgram ClassName](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Lägg till Aspose.ThreeD.Render.Shadervariabel klass](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Lägger till en Enumklass Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Lägger till buffertprogrammen](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Lägger till ett gränssnitt Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Lägger till gränssnitt Aspose.ThreeD.Render.IIndexBuffer/IVertexBufferName](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Lägger till ett enum Aspose.ThreeD.Render.IndexDataTypeName](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Lägger till teckningsprogrammen](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Lägger till ett gränssnitt Aspose.ThreeD.Render.IRenderbar.](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Lagt till ett enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Lägger till ett enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Lägger till Aspose.ThreeD.Render.RenderResource Class.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Lägger till Aspose.ThreeD.Render.RenderableResource Class.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Lägger till Aspose.ThreeD.Entites.ManualEntity Class.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Lägger till flera triangulate metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Lägger till CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState och CreateShaderProgram Metoder i Aspose.ThreeD. Render. RenderFactory-klass](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Lägger till BindRenderState, Drandexed, Draw och skickar inRenderTask-metoder i Aspose.ThreeD. Render. Hållarklass](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Lägger till RenderStage och Shader egenskaper i Aspose.ThreeD.Render.Renderer klass](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Detta dokument beskriver ändringar i Aspose.3D API från version 2.0.0 till 2.1. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteende bakom kulisserna i Aspose.3D.

{{% /alert %}} 
### **Lägger till export av Collada filer**
Med denna senaste version (2.1.0) kan utvecklare exportera Collada 3D filer. I den föregående versionen (2.0.0), har vi redan lagt till dess importfunktion, eftersom utvecklare också kan konvertera en Collada fil till andra stödda 3D filformat.
### **Lägger till ladda och spara alternativ för 3D Filformat**
Vi har lagt till laddning och spara alternativ för varje filformat. De är omverkade från de ursprungliga IOConfig-underklasserna.
#### **Lägger till Aspose.ThreeD. Format.ColladaSaveOptions klass**
Den definierar inställningar för att spara en Collada 3D fil.

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
#### **Lägger till Aspose.ThreeD. Format.Discreet3DSLoadOptions ClassName**
Det definierar inställningar på att ladda en diskret 3DS-fil.

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
#### **Lägger till Aspose.ThreeD.Formats.Discreet3DSSaveOptions ClassName**
Det definierar inställningar för att spara en diskret 3DS fil.

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
#### **Lägger till Aspose.ThreeD. Format.FBXSaveOptions ClassName**
Den definierar inställningar för att spara en FBX fil.

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
#### **Lägger till Aspose.ThreeD. Format.ObjLoadOptions ClassName**
Det definierar inställningar vid att ladda en Obj-fil.

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
#### **Lägger till Aspose.ThreeD. Format.**
Det definierar inställningar för att spara en Obj-fil.

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
#### **Lägger till Aspose.ThreeD. Format.STLLoadOptions ClassName**
Den definierar inställningar på att ladda en STL-fil.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.STLSaveOptions ClassName**
Den definierar inställningar för att spara en STL fil.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.U3DLoadOptions ClassName**
Den definierar inställningar på att ladda en U3D-fil.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.U3DSaveOptions ClassName**
Det definierar inställningar för att spara en U3D fil.

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
### **Lägger till metoder till Aspose.ThreeD.Scenklass**
Vi har överbelastat Öppna och Spara metoder i Sceneklassen. Utvecklare kan skicka ett strömobjekt eller direkt filnamn för att importera/exportera en 3D fil med hjälp av de olika laddning/sparande Valmöjligheter.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Avlägsnande av FillDummyIndexArray egendom från Aspose.ThreeD.Formats.FBXConfig klass**
Den här egendomen användes inte.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Detektera typ av en 3D- fil**
Detektera metoden för Aspose.ThreeD.FileFormat klassen kan känna igen typ av alla stöds 3D fil.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Lägger till detektera, CreateLoadOptions och CreateSaveOptions metoder i Aspose.ThreeD.**
Efter erkännande av en filtyp 3D, utvecklare kan skapa objekt LoadOptions och SaveOptions för de ytterligare manipulationsuppgifterna.

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
### **Lägger exkluderade egendom till Aspose.ThreeD.Enhet och Aspose.ThreeD.Node Klasser**
Det gör det möjligt att avlägsna ett företag under exporten.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Lägger till Aspose.ThreeD. Render. RenderState Class och Aspose.ThreeD. Render. BlådFactor/ Jämförelse/CullFaceMode/FrontFace/PolygonMode / Stencils**
Renderingstillstånden ger parametrar för GPU att rasterisera trianglar i bildpunkter.

{{% alert color="primary" %}} 

Inkapsling av hårdvara render tillstånd, detaljerad information finns på dokumentation av[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx)[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) och aspx[Vulkan Ordförande](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Lägger till Shader- API:**
Shader-programmen definierar hur trianglarna från världsutrymme ska omvandlas till skärm och beräkna den slutliga pixelfärgen i GPU- sidan ..
#### **Lägger till en abstrakt klass Aspose.ThreeD. Render. SkådareKälla och underklass Aspose.ThreeD. Render.GLSLSource**
GLSSource berättar renderare, källkoden är för OpenGL språk, den kan sammanställas till Aspose.ThreeD. Render. -ShaderProgram.
#### **Lägger till Aspose.ThreeD.Render.ShaderException klass**
Shader relaterade undantag, som huvudsakligen används i shader språket kompilering och länk steget.
#### **Lägger till Aspose.ThreeD.Render.ShaderProgram ClassName**
Det är det kompilerade shaderprogrammet.
#### **Lägg till Aspose.ThreeD.Render.Shadervariabel klass**
Den definierar de variabler som används i shader.
#### **Lägger till en Enumklass Aspose.ThreeD.Render.VariableSemantic**
Det används för att identifiera skuggarvariablens semantiska, Aspose.3D render automatiskt förbereder variabla värden beror på semantik.
### **Lägger till buffertprogrammen**
Buffertarna ger definition och data för trianglarna.
#### **Lägger till ett gränssnitt Aspose.ThreeD.Render.IBuffer**
Det är basgränssnittet för IIndexBuffer och IVertexBuffer.
#### **Lägger till gränssnitt Aspose.ThreeD.Render.IIndexBuffer/IVertexBufferName**
De presenterar maskinvarubuffertar för lagring av geometriindexen.
#### **Lägger till ett enum Aspose.ThreeD.Render.IndexDataTypeName**
Geometriindexens datatyp.
### **Lägger till teckningsprogrammen**
#### **Lägger till ett gränssnitt Aspose.ThreeD.Render.IRenderbar.**
Ett objekt som stöder rendering bör implementera detta gränssnitt.
#### **Lagt till ett enum Aspose.ThreeD.Render.DrawOperation**
Den primitiva typen att rita.
#### **Lägger till ett enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API använder renderingskö för att hantera renderingsarbetsflödet, detta används för att skicka in uppritning till angiven renderingskö.
#### **Lägger till Aspose.ThreeD.Render.RenderResource Class.**
Basklass för att överbrygga Aspose.3D:s modell API till hårdvarresurser, detta används av Aspose.3D internt, men utsätts för att släppa lös full kraft av Aspose.3D rendering.
#### **Lägger till Aspose.ThreeD.Render.RenderableResource Class.**
En underklass av RenderResource, men koncentrera dig på återgivning.
#### **Lägger till Aspose.ThreeD.Entites.ManualEntity Class.**
Användaren bör använda denna klass för att implementera sin egen enhet som stöder rendering, Denna klass inkapslar uppgifter om rendering och resurshantering.
### **Lägger till flera triangulate metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.**
Fler överbelastningar för att förenkla användningen av originalfunktionen.

**C#**

{{< highlight "csharp" >}}

 public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[]polygon);

public static int[][]Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Lägger till CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState och CreateShaderProgram Metoder i Aspose.ThreeD. Render. RenderFactory-klass**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Lägger till BindRenderState, Drandexed, Draw och skickar inRenderTask-metoder i Aspose.ThreeD. Render. Hållarklass**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Lägger till RenderStage och Shader egenskaper i Aspose.ThreeD.Render.Renderer klass**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
