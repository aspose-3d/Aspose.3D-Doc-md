---
title: Public API hangمعلقة في Aspose.3D 2.1.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Contents Sأوماري**

- [Adds Export من Collada iles](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [Ptions dds ooad و Save ptions ptions ل 3D File ororالحصير](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
  - [Adds Aspose.ThreeD](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
  - [Adds Aspose.ThreeD. orormat. Discreet3Dptions ptions oadOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
  - [Adds Aspose.ThreeD. orormat. Discreet3Dptions ptions aveOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
  - [Adds Aspose.ThreeD. orormat. ForXptions aveOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
  - [Adds Aspose.ThreeD. orormat. ObjLoadOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
  - [Adds Aspose.ThreeD. orormat. ObjSaveOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
  - [Adds Aspose.ThreeD. ororالحصير. STptions ooadOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
  - [Adds Aspose.ThreeD. orormat. SorLptions aveOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
  - [Adds Aspose.ThreeD. orormat. U3Dptions oadOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
  - [Adds Aspose.ThreeD. orormat. U3Dptions aveOptions lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [Adds Methods إلى Aspose.ThreeD. cenسينا lass](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [Removal من FillDummyIndexArray roroperty من Aspose.ThreeD. orormat. FBonononfig lass](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [Detect ype من 3D ile ile](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
  - [Ptions dds Detect ، ptions reateLoadOptions و rereateSaveOptions في Aspose.ThreeD. 07ileFormat lass](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [Adds Expackded roroperty إلى Aspose.ThreeD.Entity و Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [Adds Aspose.ThreeD](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Adds ader hader APIs](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
  - [Adds فئة مجردة Aspose.ThreeD. ender ender. hadhaderSource والفئة الفرعية Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
  - [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
  - [Adds Aspose.ThreeD. ender ender. hadhadrogram lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
  - [Add Aspose.ThreeD. ender ender. hadhaderVariable lass](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
  - [Adds و Eنوم lass لاس Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Aدس ffer ffer ffer PIs](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
  - [Adds و 07nterface Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
  - [Adds nnterfaces Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
  - [Adds و Eنوم Aspose.ThreeD. ender اندر. nndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Adds ender ender ender Is](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
  - [Adds و 07nterface Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
  - [Added an nnum Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
  - [Adds و Enum Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
  - [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
  - [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
  - [Adds Aspose.ThreeD. nntities. ManualEntity lass](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [Thodds Multiple riريانغتوال ثود في Aspose.ThreeD. nntities.](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds rereateVertexBuyee ، CreateIndexBuvec، CreateTextureUnit ، CreateRenderState و rereateShaerProgram Methods في Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [Adds indindRenderState ، DrouIndexed ، Dالخام و uubmitRenderTاسأل thoethods في Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [Adds enenderSage و Shader roroperties في Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 2.0.0 إلى 2.1.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Adds Export من Collada iles**
Uالغناء هذا الإصدار الأخير (2.1.0) ، يمكن للمطورين تصدير الملفات Collada 3D. In الإصدار السابق (2.0.0) ، لقد أضفنا بالفعل ميزة الاستيراد ، حيث يمكن للمطورين أيضا تحويل ملف Collada إلى تنسيقات الملفات الأخرى المدعومة 3D.
### **Ptions dds ooad و Save ptions ptions ل 3D File ororالحصير**
Added e قد أضاف تحميل وحفظ الخيارات لكل تنسيق ملف. يتم إعادة النظر في hey من الطبقات الفرعية الأصلية Ihey ononfig.
#### **Adds Aspose.ThreeD**
It يحدد الإعدادات على حفظ ملف Collada 3D.

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
#### **Adds Aspose.ThreeD. orormat. Discreet3Dptions ptions oadOptions lass**
It يحدد الإعدادات على تحميل ملف حصيف 3DS.

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
#### **Adds Aspose.ThreeD. orormat. Discreet3Dptions ptions aveOptions lass**
It يحدد الإعدادات على حفظ ملف حصيف 3DS.

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
#### **Adds Aspose.ThreeD. orormat. ForXptions aveOptions lass**
It يحدد الإعدادات على حفظ ملف FBX.

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
#### **Adds Aspose.ThreeD. orormat. ObjLoadOptions lass**
It يحدد الإعدادات على تحميل ملف bj O.

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
#### **Adds Aspose.ThreeD. orormat. ObjSaveOptions lass**
It يحدد الإعدادات على حفظ ملف bj O.

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
#### **Adds Aspose.ThreeD. ororالحصير. STptions ooadOptions lass**
It يحدد الإعدادات على تحميل ملف STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orormat. SorLptions aveOptions lass**
It يحدد الإعدادات على حفظ ملف STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orormat. U3Dptions oadOptions lass**
It يحدد الإعدادات على تحميل ملف U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[]{ @"c:\temp\" });

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orormat. U3Dptions aveOptions lass**
It يحدد الإعدادات على حفظ ملف U3D.

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
### **Adds Methods إلى Aspose.ThreeD. cenسينا lass**
We لديها الزائد القلم Oوطرق ave ave في فئة cenسين. Dإيفليرز يمكن تمرير كائن تيار أو اسم الملف المباشر لاستيراد/تصدير ملف 3D باستخدام مختلف خيارات التحميل/الادخار.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
### **Removal من FillDummyIndexArray roroperty من Aspose.ThreeD. orormat. FBonononfig lass**
Tلم يتم استخدام ممتلكاته.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
### **Detect ype من 3D ile ile**
The Detect طريقة Aspose.ThreeD.FileFormat فئة يمكن التعرف على نوع أي ملف معتمد 3D.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
#### **Ptions dds Detect ، ptions reateLoadOptions و rereateSaveOptions في Aspose.ThreeD. 07ileFormat lass**
After التعرف على نوع ملف 3D ، يمكن للمطورين إنشاء ptions oadOو ptions aveOالأشياء للحصول على مزيد من مهام التلاعب.

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
### **Adds Expackded roroperty إلى Aspose.ThreeD.Entity و Aspose.ThreeD.**
يسمح It بإزالة كيان أثناء التصدير.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
### **Adds Aspose.ThreeD**
Tانه يجعل الدول توفر المعلمات ل GPU لتمزيق مثلثات إلى بكسل.

{{% alert color="primary" %}} 

Encapsulation من الأجهزة تجعل الدول ، يمكن العثور على معلومات تفصيلية في وثائق[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Assx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). اسبكس) و[Vأولكان](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Adds ader hader APIs**
The Shader AIIs تحديد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU.
#### **Adds فئة مجردة Aspose.ThreeD. ender ender. hadhaderSource والفئة الفرعية Aspose.ThreeD.**
The GLSource ource يقول ren، رمز المصدر هو لغة التظليل OpenGL ، ويمكن تجميعها إلى Aspose.ThreeD.
#### **Adds Aspose.ThreeD.**
Tانه Sهادر الاستثناءات ذات الصلة ، وتستخدم أساسا في لغة شادر تجميع وربط المرحلة.
#### **Adds Aspose.ThreeD. ender ender. hadhadrogram lass**
It هو برنامج shader مجمعة.
#### **Add Aspose.ThreeD. ender ender. hadhaderVariable lass**
It يحدد المتغيرات المستخدمة في شادر.
#### **Adds و Eنوم lass لاس Aspose.ThreeD.**
يستخدم It لتحديد الدلالي متغير شادر ، Aspose.3D المستأجر إعداد القيم المتغيرة شادر تلقائيا يعتمد على الدلالات.
### **Aدس ffer ffer ffer PIs**
Tهو المخازن المؤقتة توفير تعريف والبيانات من المثلثات.
#### **Adds و 07nterface Aspose.ThreeD.**
It هو واجهة قاعدة ل InndexBuyee و ererertexBuvec.
#### **Adds nnterfaces Aspose.ThreeD.**
Hey يا مخازن الأجهزة الحالية لتخزين مؤشرات الهندسة.
#### **Adds و Eنوم Aspose.ThreeD. ender اندر. nndexDataType**
Tانه datatype من مؤشرات الهندسة.
### **Adds ender ender ender Is**
#### **Adds و 07nterface Aspose.ThreeD.**
An الكائن الذي يدعم تقديم يجب تنفيذ هذه الواجهة.
#### **Added an nnum Aspose.ThreeD.**
Tانه نوع بدائي لرسم.
#### **Adds و Enum Aspose.ThreeD.**
Aspose.3D API يستخدم طابور تقديم لإدارة سير العمل ، ويستخدم هذا لتقديم عملية تقديم إلى قائمة انتظار تقديم محددة.
#### **Adds Aspose.ThreeD.**
فئة ase briلربط طراز Aspose.3D API بموارد الأجهزة ، يتم استخدام هذا من قبل Aspose.3D داخليًا ، ولكنه يتعرض لإطلاق العنان للقوة الكاملة لعرض Aspose.3D.
#### **Adds Aspose.ThreeD.**
A Sub فئة من RenderResource ، ولكن التركيز على تقديم.
#### **Adds Aspose.ThreeD. nntities. ManualEntity lass**
Tيجب على المستخدم استخدام هذه الفئة لتنفيذ كيانها الخاص الذي يدعم تقديم ، هذه الفئة تغليف تفاصيل تقديم العمليات وإدارة الموارد.
### **Thodds Multiple riريانغتوال ثود في Aspose.ThreeD. nntities.**
Mخام الزائد لتبسيط استخدام الوظيفة الأصلية.

**C#**

{{< highlight "csharp" >}}

 public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][]Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[]polygon);

public static int[][]Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
### **Adds rereateVertexBuyee ، CreateIndexBuvec، CreateTextureUnit ، CreateRenderState و rereateShaerProgram Methods في Aspose.ThreeD.**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
### **Adds indindRenderState ، DrouIndexed ، Dالخام و uubmitRenderTاسأل thoethods في Aspose.ThreeD.**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
### **Adds enenderSage و Shader roroperties في Aspose.ThreeD.**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
