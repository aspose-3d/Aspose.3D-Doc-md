---
title: Öffentliche API Änderungen in Aspose.3D 2.1.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Inhalts übersicht**

- [Fügt den Export von Dateien Collada hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Fügt Lade-und Speichere optionen für 3D-Dateiformate hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Fügt Aspose.ThreeD. Formate. Collada SaveOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Fügt Aspose.ThreeD. Formate hinzu. Discreet3DSLoadOptions-Klasse](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Fügt Aspose.ThreeD. Formate hinzu. Discreet3DSSaveOptions-Klasse](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. FBXSaveOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. ObjLoad Options-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. ObjSaveOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. STLLoad Options-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. STL SaveOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. U3DLoadOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Fügt Aspose.ThreeD. Formate. U3DSaveOptions-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Fügt Methoden zu Aspose.ThreeD hinzu. Szenen klasse](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Entfernung der FillDummy IndexArray-Eigenschaft von Aspose.ThreeD. Formate. FBXConfig-Klasse](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Erkennen Sie den Typ einer Datei 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Fügt Detect, Create Load Options und CreateSaveOptions-Methoden in der Aspose.ThreeD.FileFormat-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Fügt Aspose.ThreeD. Entität und Aspose.ThreeD. Knoten klassen aus geschlossene Eigenschaft hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Fügt Aspose.ThreeD.Render.Render State Class und Aspose.ThreeD.Render.Blend Factor/Compare Function/CullFaceMode/Front Face/Polygon Mode/Stencil Action/Stencil State Enums hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Fügt Shader-APIs hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Fügt eine abstrakte Klasse Aspose.ThreeD hinzu. Render.Shader Source und Unter klasse Aspose.ThreeD.Render.GLSL Source](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Fügt Aspose.ThreeD.Render.Shader Exception-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Fügt Aspose.ThreeD.Render.Shader Program-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Aspose.ThreeD.Render.Shader Variable Klasse hinzufügen](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Fügt eine Enum-Klasse Aspose.ThreeD.Render.Variable Semantic hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Fügt Puffer-APIs hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Fügt eine Schnitts telle Aspose.ThreeD.Render.IBuffer hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Fügt Schnitts tellen Aspose.ThreeD. Rendern. IIndex Buffer/IVertex Buffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Fügt ein Enum Aspose.ThreeD.Render.Index Data Type hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Fügt Render-APIs hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Fügt eine Schnitts telle Aspose.ThreeD.Render. Irenderable hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Enum Aspose.ThreeD.Render.Draw Operation hinzugefügt](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Fügt eine Enum Aspose.ThreeD.Render.Render Queue GroupId hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Fügt Aspose.ThreeD.Render.RenderResource-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Fügt Aspose.ThreeD.Render.Renderable Resource-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Fügt Aspose.ThreeD. Entitäten. Manuelle Entität klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Fügt mehrere Triangulat-Methoden in der Aspose.ThreeD. Entitäten. Polygon Modifikator klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Fügt Create Vertex Buffer-, Create Index Buffer-, Create Texture Unit-, Create RenderS tate-und CreateShader Program-Methoden in der Aspose.ThreeD.Render.RenderFactory-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Fügt BindRender State-, Draw Indexed-, Draw-und Submit RenderTask-Methoden in der Aspose.ThreeD.Render.Renderer-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Fügt RenderS tage-und Shader-Eigenschaften in der Aspose.ThreeD.Render.Renderer-Klasse hinzu](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 2.0.0 bis 2.1.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Fügt den Export von Dateien Collada hinzu**
Mit dieser aktuellen Version (2.1.0) können Entwickler Collada 3D-Dateien exportieren. In der vorherigen Version (2.0.0) haben wir bereits die Import funktion hinzugefügt, da Entwickler auch eine Collada-Datei in andere unterstützte 3D-Dateiformate konvertieren können.
### **Fügt Lade-und Speichere optionen für 3D-Dateiformate hinzu**
Wir haben Lade-und Speicher optionen für jedes Dateiformat hinzugefügt. Sie werden aus den ursprünglichen IOConfig-Unter klassen neu erstellt.
#### **Fügt Aspose.ThreeD. Formate. Collada SaveOptions-Klasse hinzu**
Es definiert Einstellungen zum Speichern einer Collada 3D-Datei.

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
#### **Fügt Aspose.ThreeD. Formate hinzu. Discreet3DSLoadOptions-Klasse**
Es definiert Einstellungen zum Laden einer diskreten 3DS-Datei.

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
#### **Fügt Aspose.ThreeD. Formate hinzu. Discreet3DSSaveOptions-Klasse**
Es definiert Einstellungen zum Speichern einer diskreten 3DS-Datei.

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
#### **Fügt Aspose.ThreeD. Formate. FBXSaveOptions-Klasse hinzu**
Es definiert Einstellungen zum Speichern einer FBX-Datei.

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
#### **Fügt Aspose.ThreeD. Formate. ObjLoad Options-Klasse hinzu**
Es definiert Einstellungen zum Laden einer Obj-Datei.

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
#### **Fügt Aspose.ThreeD. Formate. ObjSaveOptions-Klasse hinzu**
Es definiert Einstellungen zum Speichern einer Obj-Datei.

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
#### **Fügt Aspose.ThreeD. Formate. STLLoad Options-Klasse hinzu**
Es definiert Einstellungen zum Laden einer STL-Datei.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Fügt Aspose.ThreeD. Formate. STL SaveOptions-Klasse hinzu**
Es definiert Einstellungen zum Speichern einer STL-Datei.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Fügt Aspose.ThreeD. Formate. U3DLoadOptions-Klasse hinzu**
Es definiert Einstellungen zum Laden einer U3D-Datei.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Fügt Aspose.ThreeD. Formate. U3DSaveOptions-Klasse hinzu**
Es definiert Einstellungen zum Speichern einer U3D-Datei.

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
### **Fügt Methoden zu Aspose.ThreeD hinzu. Szenen klasse**
Wir haben Open and Save-Methoden in der Scene-Klasse überlastet. Entwickler können ein Stream-Objekt oder einen direkten Dateinamen übergeben, um eine 3D-Datei mit den verschiedenen Lade-/Speicher optionen zu importieren/zu exportieren.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Entfernung der FillDummy IndexArray-Eigenschaft von Aspose.ThreeD. Formate. FBXConfig-Klasse**
Diese Eigenschaft wurde nicht genutzt.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Erkennen Sie den Typ einer Datei 3D**
Die Detect-Methode der Aspose.ThreeD.FileFormat-Klasse kann den Typ jeder unterstützten 3D-Datei erkennen.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Fügt Detect, Create Load Options und CreateSaveOptions-Methoden in der Aspose.ThreeD.FileFormat-Klasse hinzu**
Nach der Erkennung eines Dateityps 3D können Entwickler Load Options-und SaveOptions-Objekte für die weiteren Manipulation aufgaben erstellen.

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
### **Fügt Aspose.ThreeD. Entität und Aspose.ThreeD. Knoten klassen aus geschlossene Eigenschaft hinzu**
Dadurch kann eine Entität während des Exports entfernt werden.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Fügt Aspose.ThreeD.Render.Render State Class und Aspose.ThreeD.Render.Blend Factor/Compare Function/CullFaceMode/Front Face/Polygon Mode/Stencil Action/Stencil State Enums hinzu**
Die Render zustände bieten Parameter für die GPU zum Rastern von Dreiecken in Pixel.

{{% alert color="primary" %}} 

Kapselung von Hardware-Render zuständen, Detail informationen finden Sie in der Dokumentation von[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) und[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Fügt Shader-APIs hinzu**
Die Shader-APIs definieren, wie die Dreiecke aus dem Weltraum in den Bildschirm raum umgewandelt und die endgültige Pixel farbe auf der GPU-Seite berechnet werden.
#### **Fügt eine abstrakte Klasse Aspose.ThreeD hinzu. Render.Shader Source und Unter klasse Aspose.ThreeD.Render.GLSL Source**
Der GLSLS Source teilt dem Renderer mit, dass der Quellcode für die Schattierung sprache OpenGL gilt und auf Aspose.ThreeD.Render.Shader Program kompiliert werden kann.
#### **Fügt Aspose.ThreeD.Render.Shader Exception-Klasse hinzu**
Die Shader-bezogenen Ausnahmen, die haupt sächlich in der Kompilierung-und Verknüpfung phase der Shader-Sprache verwendet werden.
#### **Fügt Aspose.ThreeD.Render.Shader Program-Klasse hinzu**
Es ist das kompilierte Shader-Programm.
#### **Aspose.ThreeD.Render.Shader Variable Klasse hinzufügen**
Es definiert die im Shader verwendeten Variablen.
#### **Fügt eine Enum-Klasse Aspose.ThreeD.Render.Variable Semantic hinzu**
Es wird verwendet, um die semantische Shader-Variable zu identifizieren. Aspose.3D Renderer bereitet automatisch Shader-Variablen werte vor, die von der Semantik abhängen.
### **Fügt Puffer-APIs hinzu**
Die Puffer liefern Definition und Daten der Dreiecke.
#### **Fügt eine Schnitts telle Aspose.ThreeD.Render.IBuffer hinzu**
Es ist die Basis schnitts telle für IIndex Buffer und IVertex Buffer.
#### **Fügt Schnitts tellen Aspose.ThreeD. Rendern. IIndex Buffer/IVertex Buffer**
Sie präsentieren Hardware puffer zum Speichern der Geometrie indizes.
#### **Fügt ein Enum Aspose.ThreeD.Render.Index Data Type hinzu**
Der Datentyp der Geometrie indizes.
### **Fügt Render-APIs hinzu**
#### **Fügt eine Schnitts telle Aspose.ThreeD.Render. Irenderable hinzu**
Ein Objekt, das Rendering unterstützt, sollte diese Schnitts telle implemen tieren.
#### **Enum Aspose.ThreeD.Render.Draw Operation hinzugefügt**
Der primitive Typ zu zeichnen.
#### **Fügt eine Enum Aspose.ThreeD.Render.Render Queue GroupId hinzu**
Aspose.3D API verwendet die Render warteschlange, um den Render workflow zu verwalten. Dies wird verwendet, um den Render vorgang an die angegebene Render warteschlange zu senden.
#### **Fügt Aspose.ThreeD.Render.RenderResource-Klasse hinzu**
Die Basis klasse zur Überbrückung des Modells Aspose.3D des Aspose.3D mit Hardware ressourcen wird von Aspose.3D intern verwendet, kann jedoch die volle Leistung des Renderings Aspose.3D entfesseln.
#### **Fügt Aspose.ThreeD.Render.Renderable Resource-Klasse hinzu**
Eine Unterklasse von Render Resource, aber konzentrieren Sie sich auf das Rendern.
#### **Fügt Aspose.ThreeD. Entitäten. Manuelle Entität klasse hinzu**
Der Benutzer sollte diese Klasse verwenden, um eine eigene Entität zu implemen tieren, die das Rendern unterstützt. Diese Klasse kapselt die Details der Rendering-Operationen und der Ressourcen verwaltung.
### **Fügt mehrere Triangulat-Methoden in der Aspose.ThreeD. Entitäten. Polygon Modifikator klasse hinzu**
Mehr Überlastungen, um die Verwendung der ursprünglichen Funktion zu vereinfachen.

**C#**

{{< highlight "csharp" >}}

 public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[]polygon);

public static int[][]Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Fügt Create Vertex Buffer-, Create Index Buffer-, Create Texture Unit-, Create RenderS tate-und CreateShader Program-Methoden in der Aspose.ThreeD.Render.RenderFactory-Klasse hinzu**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Fügt BindRender State-, Draw Indexed-, Draw-und Submit RenderTask-Methoden in der Aspose.ThreeD.Render.Renderer-Klasse hinzu**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Fügt RenderS tage-und Shader-Eigenschaften in der Aspose.ThreeD.Render.Renderer-Klasse hinzu**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
