---
title: Публичные API Изменения в Aspose.3D 2.1.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Содержание Резюме**

- [Добавляет экспорт файлов Collada](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Добавляет параметры загрузки и сохранения для форматов файлов 3D](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Добавляет Aspose.ThreeD. Форматы. Класс ColladaSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Добавляет Aspose.ThreeD. Форматы. Класс Discreet3DSLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Добавляет Aspose.ThreeD. Форматы. Класс Discreet3DSSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Добавляет Aspose.ThreeD.Formats. Класс FBXSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Добавляет Aspose.ThreeD. Форматы. Класс ObjLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Добавляет Aspose.ThreeD. Форматы. Класс ObjSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Добавляет Aspose.ThreeD.Formats. Класс STLLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Добавляет Aspose.ThreeD.Formats. Класс STLSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Добавляет Aspose.ThreeD. Форматы. Класс U3DLoadOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Добавляет Aspose.ThreeD. Класс форматов. U3DSaveOptions](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Добавляет методы к классу сцены Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Удаление свойства FillDummyIndexArray из класса Aspose.ThreeD.Formats.FBXConfig](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Обнаружить тип файла 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Добавляет методы обнаружения, CreateLoadOptions и CreateSaveOptions в класс Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Добавляет исключенное свойство к классам Aspose.ThreeD.Entity и Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Добавлены Aspose.ThreeD. RenderState Class и Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Добавляет Shader API](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Добавляет абстрактный класс Aspose.ThreeD.Render.ShaderSource и подкласс Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Добавляет Aspose.ThreeD.Render. Класс исключения ShaderException](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Добавляет Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Добавить Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Добавляет класс Enum Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Добавляет API буфера](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Добавляет интерфейс Aspose.ThreeD.Render.IBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Добавляет интерфейсы Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Добавляет Enum Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Добавляет API-интерфейс Render](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Добавляет интерфейс Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Добавлен Enum Aspose.ThreeD.Render.DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Добавляет Enum Aspose.ThreeD.Render.RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Добавляет Aspose.ThreeD.Render.RenderResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Добавляет Aspose.ThreeD.Render.RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Добавляет Aspose.ThreeD.Entities.ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Добавляет несколько методов триангуляции в класс Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Добавляет методы CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState и CreateShaderProgram в класс Aspose.ThreeD.Render.RenderFactory](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Добавляет методы BindRenderState, Drawindexed, Draw и SubmitRenderTask в класс Aspose.ThreeD. Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Добавляет свойства RenderStage и Shader в класс Aspose.ThreeD.Render.Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API от версии 2.0.0 до 2.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
### **Добавляет экспорт файлов Collada**
Используя эту последнюю версию (2.1.0), разработчики могут экспортировать файлы Collada 3D. В предыдущей версии (2.0.0) мы уже добавили его функцию импорта, так как разработчики также могут конвертировать файл Collada в другие поддерживаемые форматы файлов 3D.
### **Добавляет параметры загрузки и сохранения для форматов файлов 3D**
Мы добавили параметры загрузки и сохранения для каждого формата файла. Они взяты из исходных подклассов IOConfig.
#### **Добавляет Aspose.ThreeD. Форматы. Класс ColladaSaveOptions**
Он определяет настройки сохранения файла Collada 3D.

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
#### **Добавляет Aspose.ThreeD. Форматы. Класс Discreet3DSLoadOptions**
Он определяет настройки при загрузке незаметного файла 3DS.

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
#### **Добавляет Aspose.ThreeD. Форматы. Класс Discreet3DSSaveOptions**
Он определяет настройки сохранения незаметного файла 3DS.

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
#### **Добавляет Aspose.ThreeD.Formats. Класс FBXSaveOptions**
Он определяет настройки сохранения файла FBX.

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
#### **Добавляет Aspose.ThreeD. Форматы. Класс ObjLoadOptions**
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

loadObjOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Добавляет Aspose.ThreeD. Форматы. Класс ObjSaveOptions**
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

saveObjOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

// serialize W component in model's vertex position

saveObjOpts.SerializeW = true;

// generate comments for each section

saveObjOpts.Verbose = true;

{{< /highlight >}}
#### **Добавляет Aspose.ThreeD.Formats. Класс STLLoadOptions**
Он определяет настройки при загрузке файла STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Добавляет Aspose.ThreeD.Formats. Класс STLSaveOptions**
Он определяет настройки сохранения файла STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Добавляет Aspose.ThreeD. Форматы. Класс U3DLoadOptions**
Он определяет настройки при загрузке файла U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Добавляет Aspose.ThreeD. Класс форматов. U3DSaveOptions**
Он определяет настройки сохранения файла U3D.

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
### **Добавляет методы к классу сцены Aspose.ThreeD.**
Мы перегрузили методы Open и Save в классе Scene. Разработчики могут передавать потоковый объект или прямое имя файла для импорта/экспорта файла 3D, используя различные параметры загрузки/сохранения.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Удаление свойства FillDummyIndexArray из класса Aspose.ThreeD.Formats.FBXConfig**
Это свойство не использовалось.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Обнаружить тип файла 3D**
Метод Detect класса Aspose.ThreeD.FileFormat может распознавать тип любого поддерживаемого файла 3D.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Добавляет методы обнаружения, CreateLoadOptions и CreateSaveOptions в класс Aspose.ThreeD.FileFormat**
После распознавания типа файла 3D разработчики могут создавать объекты LoadOptions и SaveOptions для дальнейших задач манипуляции.

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
### **Добавляет исключенное свойство к классам Aspose.ThreeD.Entity и Aspose.ThreeD.Node**
Это позволяет удалить объект во время экспорта.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Добавлены Aspose.ThreeD. RenderState Class и Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums**
Состояния рендеринга предоставляют параметры для графического процессора для растеризации треугольников в пиксели.

{{% alert color="primary" %}} 

Инкапсуляция аппаратных состояний рендеринга, подробная информация может быть найдена в документации[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) и[Вулкан](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Добавляет Shader API**
API Shader определяют, как преобразовать треугольники из мирового пространства в экранное пространство и вычислить окончательный цвет пикселя на стороне GPU.
#### **Добавляет абстрактный класс Aspose.ThreeD.Render.ShaderSource и подкласс Aspose.ThreeD.Render.GLSLSource**
GLSLSource сообщает рендереру, что исходный код предназначен для языка затенения OpenGL, его можно скомпилировать в Aspose.ThreeD.Render.ShaderProgram.
#### **Добавляет Aspose.ThreeD.Render. Класс исключения ShaderException**
Исключения, связанные с Шейдером, в основном используются на этапе компиляции и связывания языка шейдеров.
#### **Добавляет Aspose.ThreeD.Render.ShaderProgram Class**
Это составленная программа шейдеров.
#### **Добавить Aspose.ThreeD.Render.ShaderVariable Class**
Он определяет переменные, используемые в шейдере.
#### **Добавляет класс Enum Aspose.ThreeD.Render.VariableSemantic**
Он используется для идентификации семантической переменной шейдера, рендерер Aspose.3D автоматически подготавливает значения переменной шейдера в зависимости от семантики.
### **Добавляет API буфера**
Буферы предоставляют определение и данные треугольников.
#### **Добавляет интерфейс Aspose.ThreeD.Render.IBuffer**
Это базовый интерфейс для IIndexBuffer и IVertexBuffer.
#### **Добавляет интерфейсы Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
Они представляют аппаратные буферы для хранения индексов геометрии.
#### **Добавляет Enum Aspose.ThreeD.Render.IndexDataType**
Тип данных геометрических индексов.
### **Добавляет API-интерфейс Render**
#### **Добавляет интерфейс Aspose.ThreeD.Render.IRenderable**
Объект, который поддерживает рендеринг, должен реализовать этот интерфейс.
#### **Добавлен Enum Aspose.ThreeD.Render.DrawOperation**
Примитивный тип рисовать.
#### **Добавляет Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API использует очередь рендеринга для управления рабочим процессом рендеринга, это используется для отправки операции рендеринга в указанную очередь рендеринга.
#### **Добавляет Aspose.ThreeD.Render.RenderResource Class**
Базовый класс для связывания модели Aspose.3D API с аппаратными ресурсами, он используется Aspose.3D внутри компании, но может раскрыть всю мощность рендеринга Aspose.3D.
#### **Добавляет Aspose.ThreeD.Render.RenderableResource Class**
Подкласс RenderResource, но сосредоточьтесь на рендеринге.
#### **Добавляет Aspose.ThreeD.Entities.ManualEntity Class**
Пользователь должен использовать этот класс для реализации своего собственного объекта, который поддерживает рендеринг, этот класс инкапсулирует детали операций рендеринга и управления ресурсами.
### **Добавляет несколько методов триангуляции в класс Aspose.ThreeD.Entities.PolygonModifier**
Больше перегрузок, чтобы упростить использование оригинальной функции.

**C#**

{{< highlight "csharp" >}}

 public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[]polygon);

public static int[][]Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Добавляет методы CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState и CreateShaderProgram в класс Aspose.ThreeD.Render.RenderFactory**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Добавляет методы BindRenderState, Drawindexed, Draw и SubmitRenderTask в класс Aspose.ThreeD. Renderer**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Добавляет свойства RenderStage и Shader в класс Aspose.ThreeD.Render.Renderer**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
