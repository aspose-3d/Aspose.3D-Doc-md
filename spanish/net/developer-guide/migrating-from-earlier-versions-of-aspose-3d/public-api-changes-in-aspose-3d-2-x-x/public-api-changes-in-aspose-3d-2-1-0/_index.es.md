---
title: Público API Cambios en Aspose.3D 2.1.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Resumen de contenidos**

- [Agrega la exportación de archivos Collada](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Agrega opciones de carga y guardado para formatos de archivo 3D](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
[Agrega la clase Aspose.ThreeD.Formats.ColladaSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
[Agrega la clase Aspose.ThreeD.Formats.Discreet3DSLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.Discreet3DSSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.FBXSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.ObjLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.ObjSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.STLLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.STLSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
[Agrega la clase Aspose.ThreeD.Formats.U3DLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
[Añade la clase Aspose.ThreeD.Formats.U3DSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Agrega métodos a Aspose.ThreeD.Scene Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Eliminación de la propiedad FillDummyIndexArray de la clase Aspose.ThreeD.Formats.FBXConfig](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Detectar el tipo de archivo 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
[Agrega los métodos Detect, CreateLoadOptions y CreateSaveOptions en la clase Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Agrega la propiedad excluida a las clases Aspose.ThreeD.Entity y Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Agrega la clase Aspose.ThreeD.Render.RenderState y Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/S](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Agrega las API de Shader](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
[Agrega una clase abstracta Aspose.ThreeD.Render.ShaderSource y una subclase Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
[Agrega la clase Aspose.ThreeD.Render.ShaderException](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
[Agrega la clase Aspose.ThreeD.Render.ShaderProgram](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
[Agregar clase Aspose.ThreeD.Render.ShaderVariable](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
[Agrega una clase Enum Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Agrega API de búfer](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
[Agrega una interfaz Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
[Agrega las interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
[Agrega un Enum Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Agrega API de renderizado](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
[Agrega una interfaz Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
[Se agregó un Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
[Agrega un Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
[Agrega Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
[Agrega Aspose.ThreeD.Render.RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
[Agrega la clase Aspose.ThreeD.Entities.ManualEntity](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Agrega varios métodos Triangulate en la clase Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Agrega los métodos CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState y CreateShaderProgram en la clase Aspose.ThreeD.Render.RenderFactory](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Agrega los métodos BindRenderState, DrawIndexed, Draw y SubmitRenderTask en la clase Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Agrega las propiedades de RenderStage y Shader en la clase Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 2.0.0 to 2.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Agrega la exportación de archivos Collada**
Usando esta versión reciente (2.1.0), los desarrolladores pueden exportar archivos Collada 3D. En la versión anterior (2.0.0), ya hemos añadido su función de importación, ya que los desarrolladores también pueden convertir un archivo Collada a otros formatos de archivo 3D compatibles.
###  **Agrega opciones de carga y guardado para formatos de archivo 3D**
Hemos añadido opciones de carga y guardar para cada formato de archivo. Se refactorian de las subclases IOConfig originales.
####  **Agrega la clase Aspose.ThreeD.Formats.ColladaSaveOptions**
Define la configuración para guardar un archivo Collada 3D.

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
####  **Agrega la clase Aspose.ThreeD.Formats.Discreet3DSLoadOptions**
Define los ajustes para cargar un archivo 3DS discreto.

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
####  **Agrega la clase Aspose.ThreeD.Formats.Discreet3DSSaveOptions**
Define configuraciones para guardar un archivo 3DS discreto.

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
####  **Agrega la clase Aspose.ThreeD.Formats.FBXSaveOptions**
Define la configuración para guardar un archivo FBX.

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
####  **Agrega la clase Aspose.ThreeD.Formats.ObjLoadOptions**
Define la configuración de la carga de un archivo Obj.

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
####  **Agrega la clase Aspose.ThreeD.Formats.ObjSaveOptions**
Define la configuración para guardar un archivo Obj.

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
####  **Agrega la clase Aspose.ThreeD.Formats.STLLoadOptions**
Define los ajustes para cargar un archivo STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Agrega la clase Aspose.ThreeD.Formats.STLSaveOptions**
Define la configuración para guardar un archivo STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Agrega la clase Aspose.ThreeD.Formats.U3DLoadOptions**
Define la configuración de la carga de un archivo U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Añade la clase Aspose.ThreeD.Formats.U3DSaveOptions**
Define la configuración para guardar un archivo U3D.

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
###  **Agrega métodos a Aspose.ThreeD.Scene Class**
Hemos sobrecargado los métodos Open y Save en la clase Scene. Los desarrolladores pueden pasar un objeto de flujo o un nombre de archivo directo para importar/exportar un archivo 3D utilizando las diversas opciones de carga/guardado.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **Eliminación de la propiedad FillDummyIndexArray de la clase Aspose.ThreeD.Formats.FBXConfig**
Esta propiedad no se estaba utilizando.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **Detectar el tipo de archivo 3D**
El método Detect de la clase Aspose.ThreeD.FileFormat puede reconocer el tipo de cualquier archivo 3D admitido.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **Agrega los métodos Detect, CreateLoadOptions y CreateSaveOptions en la clase Aspose.ThreeD.FileFormat**
Después del reconocimiento de un tipo de archivo 3D, los desarrolladores pueden crear objetos LoadOptions y SaveOptions para las tareas de manipulación adicionales.

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
###  **Agrega la propiedad excluida a las clases Aspose.ThreeD.Entity y Aspose.ThreeD.Node**
Permite eliminar una entidad durante la exportación.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **Agrega la clase Aspose.ThreeD.Render.RenderState y Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/S**
Los estados de render proporcionan parámetros para que la GPU rasterice los triángulos en píxeles.

{{% alert color="primary" %}} 

Encapsulación de los estados de renderizado de hardware, la información detallada se puede encontrar en la documentación de [OpenGL 4,0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx y [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
###  **Agrega las API de Shader**
Las API de Shader definen cómo transformar los triángulos del espacio del mundo en el espacio de la pantalla y calcular el color de píxel final en el lado de la GPU.
####  **Agrega una clase abstracta Aspose.ThreeD.Render.ShaderSource y una subclase Aspose.ThreeD.Render.GLSLSource**
GLSLSSource le dice al renderizador, el código fuente es para el lenguaje de sombreado OpenGL, se puede compilar en Aspose.ThreeD.Render.ShaderProgram.
####  **Agrega la clase Aspose.ThreeD.Render.ShaderException**
Las excepciones relacionadas con Shader, utilizadas principalmente en la etapa de compilación y vinculación del lenguaje del sombreador.
####  **Agrega la clase Aspose.ThreeD.Render.ShaderProgram**
Es el programa de sombreado compilado.
####  **Agregar clase Aspose.ThreeD.Render.ShaderVariable**
Define las variables utilizadas en el sombreado.
####  **Agrega una clase Enum Aspose.ThreeD.Render.VariableSemantic**
Se utiliza para identificar la semántica de la variable de sombreado, Aspose.3D El renderizador preparará automáticamente los valores de la variable de sombreado según la semántica.
###  **Agrega API de búfer**
Los búferes proporcionan definición y datos de los triángulos.
####  **Agrega una interfaz Aspose.ThreeD.Render.IBuffer**
Es la interfaz base para IIndexBuffer e IVertexBuffer.
####  **Agrega las interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
Presentan búferes de hardware para almacenar los índices de geometría.
####  **Agrega un Enum Aspose.ThreeD.Render.IndexDataType**
El tipo de datos de los índices de geometría.
###  **Agrega API de renderizado**
####  **Agrega una interfaz Aspose.ThreeD.Render.IRenderable**
Un objeto que admita la representación debe implementar esta interfaz.
####  **Se agregó un Enum Aspose.ThreeD.Render.DrawOperation**
El tipo primitivo para dibujar.
####  **Agrega un Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API usa la cola de render para administrar el flujo de trabajo de render, esto se usa para enviar la operación de render a la cola de render especificada.
####  **Agrega Aspose.ThreeD.Render.RenderResource Class**
Clase base para unir el modelo Aspose.3D API a los recursos de hardware, esto es utilizado por Aspose.3D internamente, pero expuesto para liberar toda la potencia de la representación Aspose.3D.
####  **Agrega Aspose.ThreeD.Render.RenderableResource Class**
Una subclase de RenderResource, pero concéntrese en la renderización.
####  **Agrega la clase Aspose.ThreeD.Entities.ManualEntity**
El usuario debe usar esta clase para implementar su propia entidad que admita la representación, esta clase encapsula los detalles de las operaciones de representación y la administración de recursos.
###  **Agrega varios métodos Triangulate en la clase Aspose.ThreeD.Entities.PolygonModifier**
Más sobrecargas para simplificar el uso de la función original.

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **Agrega los métodos CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState y CreateShaderProgram en la clase Aspose.ThreeD.Render.RenderFactory**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **Agrega los métodos BindRenderState, DrawIndexed, Draw y SubmitRenderTask en la clase Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **Agrega las propiedades de RenderStage y Shader en la clase Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
