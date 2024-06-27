---
title: Variazioni pubbliche di API in Aspose.3D 2.1.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Contenuto sommario**

- [Aggiunge l'esportazione di file Collada](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Aggiunge opzioni di caricamento e salvataggio per i formati di file 3D](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
-[Aggiunge Aspose.ThreeD.Formats.ColladaSaveOptions class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
-[Aggiunge Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.FBXSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.ObjLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
-[Aggiunge Aspose. Formati ThreeD. Classe ObjSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.STLLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.STLSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.U3DLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
-[Aggiunge Aspose.ThreeD.Formats.U3DSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Aggiunge metodi a Aspose.ThreeD.Scene Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Rimozione della proprietà FillDummyIndexArray da Aspose.ThreeD.Formats.FBXConfig Class](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Rileva il tipo di file 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
-[Aggiunge Rileva, CreateLoadOptions e CreateSaveOptions Metodi nella classe Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Aggiunge la proprietà esclusa a Aspose.ThreeD. Entità e Aspose. Classi dei nodi ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Aggiunge Aspose.ThreeD.Render.RenderState Class e Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Aggiunge API Shader](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
-[Aggiunge una classe astratta Aspose.ThreeD.Render.ShaderSource e sottoclasse Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
-[Aggiunge Aspose.ThreeD.Render.ShaderException Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
-[Aggiunge Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
-[Aggiungi Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
-[Aggiunge una classe Enum Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Aggiunge API buffer](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
-[Aggiunge un'interfaccia Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
-[Aggiunge interfacce Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
-[Aggiunge un Enum Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Aggiunge le API di Render](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
-[Aggiunge un'interfaccia Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
-[Aggiunto un Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
-[Aggiunge un Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
-[Aggiunge Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
-[Aggiunge Aspose.ThreeD.Render.RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
-[Aggiunge Aspose. Entità ThreeD.. ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Aggiunge più metodi triangolati nella classe Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Aggiunge i metodi CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState e CreateShaderProgram nella classe Aspose.ThreeD.Render.RenderFactory](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Aggiunge i metodi BindRenderState, DrawIndexed, Draw e SubmitRenderTask nella classe Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Aggiunge le proprietà RenderStage e Shader nella classe Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche alla versione Aspose.3D API dalla versione 2.0.0 alla 2.1.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Aggiunge l'esportazione di file Collada**
Utilizzando questa versione recente (2.1.0), gli sviluppatori possono esportare file Collada 3D. Nella versione precedente (2.0.0), abbiamo già aggiunto la sua funzione di importazione, poiché gli sviluppatori possono anche convertire un file Collada in altri formati di file 3D supportati.
###  **Aggiunge opzioni di caricamento e salvataggio per i formati di file 3D**
Abbiamo aggiunto opzioni di carico e salvataggio per ogni formato di file. Sono rifattorizzati dalle sottoclassi IOConfig originali.
####  **Aggiunge Aspose.ThreeD.Formats.ColladaSaveOptions class**
Definisce le impostazioni sul salvataggio di un file Collada 3D.

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
####  **Aggiunge Aspose.ThreeD.Formats.Discreet3DSLoadOptions Class**
Definisce le impostazioni sul caricamento di un discreto file 3DS.

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
####  **Aggiunge Aspose.ThreeD.Formats.Discreet3DSSaveOptions Class**
Definisce le impostazioni sul salvataggio di un discreto file 3DS.

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
####  **Aggiunge Aspose.ThreeD.Formats.FBXSaveOptions Class**
Definisce le impostazioni sul salvataggio di un file FBX.

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
####  **Aggiunge Aspose.ThreeD.Formats.ObjLoadOptions Class**
Definisce le impostazioni sul caricamento di un file Obj.

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
####  **Aggiunge Aspose. Formati ThreeD. Classe ObjSaveOptions**
Definisce le impostazioni sul salvataggio di un file Obj.

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
####  **Aggiunge Aspose.ThreeD.Formats.STLLoadOptions Class**
Definisce le impostazioni sul caricamento di un file STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aggiunge Aspose.ThreeD.Formats.STLSaveOptions Class**
Definisce le impostazioni sul salvataggio di un file STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aggiunge Aspose.ThreeD.Formats.U3DLoadOptions Class**
Definisce le impostazioni sul caricamento di un file U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Aggiunge Aspose.ThreeD.Formats.U3DSaveOptions Class**
Definisce le impostazioni sul salvataggio di un file U3D.

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
###  **Aggiunge metodi a Aspose.ThreeD.Scene Class**
Abbiamo sovraccaricato i metodi Open and Save nella classe Scene. Gli sviluppatori possono passare un oggetto stream o un nome file diretto per importare/esportare un file 3D utilizzando le varie opzioni di caricamento/salvataggio.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **Rimozione della proprietà FillDummyIndexArray da Aspose.ThreeD.Formats.FBXConfig Class**
Questa proprietà non veniva utilizzata.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **Rileva il tipo di file 3D**
Il metodo Rileva della classe Aspose.ThreeD.FileFormat può riconoscere il tipo di qualsiasi file 3D supportato.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **Aggiunge Rileva, CreateLoadOptions e CreateSaveOptions Metodi nella classe Aspose.ThreeD.FileFormat**
Dopo il riconoscimento di un tipo di file 3D, gli sviluppatori possono creare oggetti LoadOptions e SaveOptions per ulteriori attività di manipolazione.

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
###  **Aggiunge la proprietà esclusa a Aspose.ThreeD. Entità e Aspose. Classi dei nodi ThreeD.**
Consente di rimuovere un'entità durante l'esportazione.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **Aggiunge Aspose.ThreeD.Render.RenderState Class e Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums**
Gli stati di rendering forniscono parametri per la GPU per rasterizzare i triangoli in pixel.

{{% alert color="primary" %}} 

Incapsulamento degli stati di rendering dell'hardware, le informazioni dettagliate sono disponibili nella documentazione di [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirettX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirettX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) e [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
###  **Aggiunge API Shader**
Le API Shader definiscono come trasformare i triangoli dallo spazio del mondo nello spazio dello schermo e calcolare il colore finale del pixel sul lato GPU.
####  **Aggiunge una classe astratta Aspose.ThreeD.Render.ShaderSource e sottoclasse Aspose.ThreeD.Render.GLSLSource**
GLSLSource dice al renderer, il codice sorgente è per il linguaggio di ombreggiatura OpenGL, può essere compilato in Aspose.ThreeD.Render.ShaderProgram.
####  **Aggiunge Aspose.ThreeD.Render.ShaderException Class**
Le eccezioni relative allo shader, utilizzate principalmente nella fase di compilazione e collegamento in lingua shader.
####  **Aggiunge Aspose.ThreeD.Render.ShaderProgram Class**
È il programma shader compilato.
####  **Aggiungi Aspose.ThreeD.Render.ShaderVariable Class**
Definisce le variabili utilizzate in shader.
####  **Aggiunge una classe Enum Aspose.ThreeD.Render.VariableSemantic**
Viene utilizzato per identificare la semantica della variabile shader, Aspose.3D renderer preparerà automaticamente i valori delle variabili shader a seconda della semantica.
###  **Aggiunge API buffer**
I buffer forniscono definizione e dati dei triangoli.
####  **Aggiunge un'interfaccia Aspose.ThreeD.Render.IBuffer**
È l'interfaccia di base per IIndexBuffer e IVertexBuffer.
####  **Aggiunge interfacce Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
Presentano buffer hardware per la memorizzazione degli indici di geometria.
####  **Aggiunge un Enum Aspose.ThreeD.Render.IndexDataType**
Il tipo di dati degli indici di geometria.
###  **Aggiunge le API di Render**
####  **Aggiunge un'interfaccia Aspose.ThreeD.Render.IRenderable**
Un oggetto che supporta il rendering dovrebbe implementare questa interfaccia.
####  **Aggiunto un Enum Aspose.ThreeD.Render.DrawOperation**
Il tipo primitivo da disegnare.
####  **Aggiunge un Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API utilizza la coda di rendering per gestire il flusso di lavoro di rendering, questo viene utilizzato per inviare l'operazione di rendering alla coda di rendering specificata.
####  **Aggiunge Aspose.ThreeD.Render.RenderResource Class**
Base class for bridging the Aspose.3D's model API to hardware resources, this is used by Aspose.3D internally, but exposed to unleash the full power of Aspose.3D rendering.
####  **Aggiunge Aspose.ThreeD.Render.RenderableResource Class**
Una sottoclasse di RenderResource, ma concentrati sul rendering.
####  **Aggiunge Aspose. Entità ThreeD.. ManualEntity Class**
L'utente deve utilizzare questa classe per implementare la propria entità che supporta il rendering, questa classe incapsula i dettagli delle operazioni di rendering e della gestione delle risorse.
###  **Aggiunge più metodi triangolati nella classe Aspose.ThreeD.Entities.PolygonModifier**
Più sovraccarichi per semplificare l'utilizzo della funzione originale.

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **Aggiunge i metodi CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState e CreateShaderProgram nella classe Aspose.ThreeD.Render.RenderFactory**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **Aggiunge i metodi BindRenderState, DrawIndexed, Draw e SubmitRenderTask nella classe Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **Aggiunge le proprietà RenderStage e Shader nella classe Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
