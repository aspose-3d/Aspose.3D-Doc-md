---
title: Публичные изменения API в Aspose.3D 2.1.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Содержание Резюме**

- [Добавление экспорта файлов Collada](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Добавляет параметры загрузки и сохранения для форматов файлов 3D](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
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
- [Добавляет методы в класс Aspose.ThreeD.Scene](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Удаление свойства FillDummyIndexArray из Aspose.ThreeD. Форматы. Класс FBXConfig](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Определение типа файла 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Adds Detect, CreateLoadOptions and CreateSaveOptions Methods in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Добавляет исключенное свойство в классы Aspose.ThreeD.Entity и Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Добавляет Aspose.ThreeD. Рендер. Класс RenderState и Aspose.ThreeD. Рендер. BlendFactor/СравнениеФункция/CullFaceMode/FrontFace/PolygonMode/StencilAction Enums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Добавляет Shader API](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Adds an abstract class Aspose.ThreeD.Render.ShaderSource and sub class Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Adds Aspose.ThreeD.Render.ShaderException Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Adds Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Add Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Adds an Enum Class Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Добавляет API буфера](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Adds an Interface Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Adds Interfaces Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Adds an Enum Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Добавляет API-интерфейс Render](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Adds an Interface Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Added an Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Adds an Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Adds Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Adds Aspose.ThreeD.Render.RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Adds Aspose.ThreeD.Entities.ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Добавляет несколько триангуляционных методов в класс Aspose.ThreeD. Enties. PolygonModifier](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Добавляет методы CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState и CreateShaderProgram в класс Aspose.ThreeD.Render.RenderFactory](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Добавление методов BindRenderState, DrawIndexed, Draw и SubmitRenderTask в класс Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Добавление свойств RenderStage и Shader в класс Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 2.0.0 до 2.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Добавление экспорта файлов Collada**
Используя эту последнюю версию (2.1.0), разработчики могут экспортировать файлы Collada 3D. В предыдущей версии (2.0.0) мы уже добавили его функцию импорта, поскольку разработчики также могут конвертировать файл Collada в другие поддерживаемые форматы файлов 3D.
###  **Добавляет параметры загрузки и сохранения для форматов файлов 3D**
Мы добавили параметры загрузки и сохранения для каждого формата файла. Они взяты из исходных подклассов IOConfig.
####  **Добавляет Aspose.ThreeD. Форматы. Класс ColladaSaveOptions**
Он определяет параметры сохранения файла Collada 3D.

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
####  **Добавляет Aspose.ThreeD. Форматы. Discreet3DSLoadOptions Класс**
Он определяет настройки при загрузке дискретного файла 3DS.

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
####  **Добавляет Aspose.ThreeD. Форматы. Discreet3DSSaveOptions Класс**
Он определяет параметры сохранения дискретного файла 3DS.

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
####  **Добавляет Aspose.ThreeD. Форматы. Класс FBXSaveOptions**
Он определяет параметры сохранения файла FBX.

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
####  **Добавляет Aspose.ThreeD. Форматы. Класс ObjLoadOptions**
Он определяет настройки при загрузке файла Obj.

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
####  **Добавляет Aspose.ThreeD. Форматы. Класс ObjSaveOptions**
Он определяет настройки при сохранении файла Obj.

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
####  **Добавляет Aspose.ThreeD. Форматы. STLLoadOptions Класс**
Он определяет настройки при загрузке файла STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Добавляет Aspose.ThreeD. Форматы. Класс STLSaveOptions**
Он определяет параметры сохранения файла STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Добавляет Aspose.ThreeD. Форматы. Класс U3DLoadOptions**
Он определяет настройки при загрузке файла U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **Добавляет Aspose.ThreeD. Форматы. Класс U3DSaveOptions**
Он определяет настройки при сохранении файла U3D.

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
###  **Добавляет методы в класс Aspose.ThreeD.Scene**
Мы перегружали методы Open и Save в классе Scene. Разработчики могут передавать потоковый объект или прямое имя файла для импорта/экспорта файла 3D, используя различные параметры загрузки/сохранения.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **Удаление свойства FillDummyIndexArray из Aspose.ThreeD. Форматы. Класс FBXConfig**
Это свойство не использовалось.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **Определение типа файла 3D**
Метод Detect класса Aspose.ThreeD.FileFormat может распознавать тип любого поддерживаемого файла 3D.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **Добавление методов обнаружения, создания LoadOptions и создания SaveOptions в класс Aspose.ThreeD.FileFormat**
После распознавания типа файла 3D разработчики могут создавать объекты LoadOptions и SaveOptions для дальнейших задач манипулирования.

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
###  **Добавляет исключенное свойство в классы Aspose.ThreeD.Entity и Aspose.ThreeD.Node**
Это позволяет удалить объект во время экспорта.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **Добавляет Aspose.ThreeD. Рендер. Класс RenderState и Aspose.ThreeD. Рендер. BlendFactor/СравнениеФункция/CullFaceMode/FrontFace/PolygonMode/StencilAction Enums**
Состояния рендеринга предоставляют параметры для графического процессора для растеризации треугольников в пиксели.

{{% alert color="primary" %}} 

Инкапсуляция аппаратных состояний рендера, подробную информацию можно найти в документации [OpenGL 4,0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) и [Вулкан](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
###  **Добавляет Shader API**
API Shader определяют, как преобразовать треугольники из мирового пространства в экранное пространство и вычислить окончательный цвет пикселя на стороне GPU.
####  **Добавляет абстрактный класс Aspose.ThreeD.Render.ShaderSource и подкласс Aspose.ThreeD.Render.GLSLSource**
GLSLSource сообщает рендереру, что исходный код предназначен для языка затенения OpenGL, он может быть скомпилирован в Aspose.ThreeD.Render.ShaderProgram.
####  **Добавляет Aspose.ThreeD. Рендер. Класс ShaderException**
Исключения, связанные с Шейдером, в основном используются на этапе компиляции и связывания языка шейдеров.
####  **Добавляет класс Aspose.ThreeD.Render.ShaderProgram**
Это составленная программа шейдеров.
####  **Добавить класс Aspose.ThreeD.Render.ShaderVariable**
Он определяет переменные, используемые в шейдере.
####  **Добавляет класс Enum Aspose.ThreeD.Render. VariableСемантический**
Он используется для определения семантики переменной шейдера, Aspose.3D рендерер автоматически подготовит значения переменной шейдера в зависимости от семантики.
###  **Добавляет API буфера**
Буферы предоставляют определение и данные треугольников.
####  **Добавление интерфейса Aspose.ThreeD.Render.IBuffer**
Это базовый интерфейс для IIndexBuffer и IVertexBuffer.
####  **Добавление интерфейсов Aspose.ThreeD.Render. IndexBuffer/IVertexBuffer**
Они представляют аппаратные буферы для хранения индексов геометрии.
####  **Добавляет Enum Aspose.ThreeD. Рендер. Тип IndexDataType**
Тип данных геометрических индексов.
###  **Добавляет API-интерфейс Render**
####  **Добавляет интерфейс Aspose.ThreeD.Render.IRenderable**
Объект, который поддерживает рендеринг, должен реализовать этот интерфейс.
####  **Добавлен Enum Aspose.ThreeD.Render.DrawOperation**
Примитивный тип рисовать.
####  **Добавляет Enum Aspose.ThreeD. Рендеринг. РендерQueueGroupId**
Aspose.3D API использует очередь рендеринга для управления процессом рендеринга, которая используется для отправки операции рендеринга в указанную очередь рендеринга.
####  **Добавляет класс Aspose.ThreeD.Render.RenderResource**
Базовый класс для соединения Aspose.3D модели API с аппаратными ресурсами, используется Aspose.3D внутренне, но может раскрыть всю мощь Aspose.3D рендеринга.
####  **Добавляет класс Aspose.ThreeD.Render.RenderableResource**
Подкласс RenderResource, но сосредоточьтесь на рендеринге.
####  **Добавляет Aspose.ThreeD. Сущности. Класс Сущностей ManualEntity**
Пользователь должен использовать этот класс для реализации своего собственного объекта, который поддерживает рендеринг, этот класс инкапсулирует детали операций рендеринга и управления ресурсами.
###  **Добавляет несколько триангуляционных методов в класс Aspose.ThreeD. Enties. PolygonModifier**
Больше перегрузок, чтобы упростить использование оригинальной функции.

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **Добавляет методы CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState и CreateShaderProgram в класс Aspose.ThreeD.Render.RenderFactory**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **Добавление методов BindRenderState, DrawIndexed, Draw и SubmitRenderTask в класс Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **Добавление свойств RenderStage и Shader в класс Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
