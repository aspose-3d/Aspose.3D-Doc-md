---
title: العام API يتغير بـ Aspose.3D 2.1.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-2-1-0/
---
**Contents Sأوماري**

- [إضافة تصدير ملفات Collada](#PublicAPIChangesinAspose.3D2.1.0-AddsExportofColladaFiles)
- [إضافة تحميل وحفظ الخيارات لتنسيقات الملفات 3D](#PublicAPIChangesinAspose.3D2.1.0-AddsLoadandSaveOptionsfor3DFileFormats) 
-[يضيف Aspose.ThreeD. Formes. ColladaSaveOptions class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ColladaSaveOptionsclass)
-[يضيف Aspose.ThreeD.Formats. Secreet3dslodutions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSLoadOptionsClass)
-[يضيف Aspose.ThreeD.Formats. Secreet3dssaveoptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.Discreet3DSSaveOptionsClass)
-[يضيف Aspose.ThreeD.Formats.FBXSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.FBXSaveOptionsClass)
-[يضيف Aspose.ThreeD.Formats.ObjLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjLoadOptionsClass)
-[يضيف Aspose.ThreeD.Formats.ObjSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.ObjSaveOptionsClass)
-[يضيف Aspose.ThreeD. Formaces. STLLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLLoadOptionsClass)
-[تضيف Aspose.ThreeD. Formes. STLSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.STLSaveOptionsClass)
-[يضيف Aspose.ThreeD. Formaces. U3DLoadOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DLoadOptionsClass)
-[يضيف Aspose.ThreeD.Formats.U3DSaveOptions Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Formats.U3DSaveOptionsClass)
- [تضيف طرقًا إلى Aspose.ThreeD.Scene Class](#PublicAPIChangesinAspose.3D2.1.0-AddsMethodstoAspose.ThreeD.SceneClass)
- [إزالة خاصية filldummyindexary من Aspose.ThreeD. Fformes. FBXConfig Class](#PublicAPIChangesinAspose.3D2.1.0-RemovalofFillDummyIndexArrayPropertyfromAspose.ThreeD.Formats.FBXConfigClass)
- [اكتشاف نوع ملف 3D](#PublicAPIChangesinAspose.3D2.1.0-DetecttheTypeofa3DFile) 
-[يضيف طرق الكشف والتبني createloadtions و CreateSaveOptions في فئة Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D2.1.0-AddsDetect,CreateLoadOptionsandCreateSaveOptionsMethodsintheAspose.ThreeD.FileFormatClass)
- [تضيف الخاصية المستبعدة إلى Aspose.ThreeD.Entity و Aspose.ThreeD.Node Classes](#PublicAPIChangesinAspose.3D2.1.0-AddsExcludedPropertytoAspose.ThreeD.EntityandAspose.ThreeD.NodeClasses)
- [يضيف Aspose.ThreeD. RenderState Class و Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/state](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderStateClassandAspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilStateEnums)
- [Adds ader hader APIs](#PublicAPIChangesinAspose.3D2.1.0-AddsShaderAPIs) 
-[يضيف فئة تجريدية Aspose.ThreeD.Render.ShaderSource والفئة الفرعية Aspose.ThreeD.Render.GLSLSource](#PublicAPIChangesinAspose.3D2.1.0-AddsanabstractclassAspose.ThreeD.Render.ShaderSourceandsubclassAspose.ThreeD.Render.GLSLSource)
-[تضيف Aspose.ThreeD.Render.ShaderException Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderExceptionClass)
-[تضيف Aspose.ThreeD.Render.ShaderProgram Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.ShaderProgramClass)
-[أضف Aspose.ThreeD.Render.ShaderVariable Class](#PublicAPIChangesinAspose.3D2.1.0-AddAspose.ThreeD.Render.ShaderVariableClass)
-[يضيف فئة قائمة Aspose.ThreeD.Render.VariableSemantic](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumClassAspose.ThreeD.Render.VariableSemantic)
- [Aدس ffer ffer ffer PIs](#PublicAPIChangesinAspose.3D2.1.0-AddsBufferAPIs) 
-[إضافة واجهة Aspose.ThreeD.Render. Ibuer](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IBuffer)
-[يضيف واجهات Aspose.ThreeD.Render. Iindexbover/ivertexbuer](#PublicAPIChangesinAspose.3D2.1.0-AddsInterfacesAspose.ThreeD.Render.IIndexBuffer/IVertexBuffer)
-[يضيف نموًا Aspose.ThreeD.Render.IndexDataType](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.IndexDataType)
- [Adds ender ender ender Is](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderAPIs) 
-[إضافة واجهة Aspose.ThreeD.Render.IRenderable](#PublicAPIChangesinAspose.3D2.1.0-AddsanInterfaceAspose.ThreeD.Render.IRenderable)
-[تمت إضافة عدد Aspose.ThreeD. Ender. DrawOperation](#PublicAPIChangesinAspose.3D2.1.0-AddedanEnumAspose.ThreeD.Render.DrawOperation)
-[يضيف إنم Aspose.ThreeD. Reender. RenderQueueGroupId](#PublicAPIChangesinAspose.3D2.1.0-AddsanEnumAspose.ThreeD.Render.RenderQueueGroupId)
-[تضيف Aspose.ThreeD. Rendersource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderResourceClass)
-[تضيف Aspose.ThreeD. RenderableResource Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Render.RenderableResourceClass)
-[تضيف Aspose.ThreeD. Forties. ManualEntity Class](#PublicAPIChangesinAspose.3D2.1.0-AddsAspose.ThreeD.Entities.ManualEntityClass)
- [تضيف طرق تثليث متعددة في فئة Aspose.ThreeD. Enties. PolygonModifier](#PublicAPIChangesinAspose.3D2.1.0-AddsMultipleTriangulateMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)
- [يضيف createvertexbuer ، creatindexbuer ، CreateTextureUnit ، createrendestate و CreateShaderProgram أساليب في Aspose.ThreeD. RenderFactory Class](#PublicAPIChangesinAspose.3D2.1.0-AddsCreateVertexBuffer,CreateIndexBuffer,CreateTextureUnit,CreateRenderStateandCreateShaderProgramMethodsintheAspose.ThreeD.Render.RenderFactoryClass)
- [تضيف طرق BindRenderState و drawinderstate و drawinded و drawing و submiderender في فئة Aspose.ThreeD. Renderer](#PublicAPIChangesinAspose.3D2.1.0-AddsBindRenderState,DrawIndexed,DrawandSubmitRenderTaskMethodsintheAspose.ThreeD.Render.RendererClass)
- [تضيف خصائص RenderStage و Shader في فئة Aspose.ThreeD.Render](#PublicAPIChangesinAspose.3D2.1.0-AddsRenderStageandShaderPropertiesintheAspose.ThreeD.Render.RendererClass)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 2.0.0 إلى 2.1.0 ، والتي قد تكون ذات فائدة لمطوري الوحدة/التطبيق. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **إضافة تصدير ملفات Collada**
باستخدام هذا الإصدار الحديث (2.1.0) ، يمكن للمطورين تصدير ملفات Collada 3D. في الإصدار السابق (2.0.0) ، أضفنا بالفعل ميزة الاستيراد الخاصة بها ، حيث يمكن للمطورين أيضًا تحويل ملف Collada إلى تنسيقات ملفات 3D أخرى مدعومة.
###  **إضافة تحميل وحفظ الخيارات لتنسيقات الملفات 3D**
Added e قد أضاف تحميل وحفظ الخيارات لكل تنسيق ملف. يتم إعادة النظر في hey من الطبقات الفرعية الأصلية Ihey ononfig.
####  **يضيف Aspose.ThreeD. Formes. ColladaSaveOptions class**
إنه يحدد الإعدادات عند حفظ ملف Collada 3D.

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
####  **يضيف Aspose.ThreeD.Formats. Secreet3dslodutions Class**
يحدد الإعدادات عند تحميل ملف 3DS غير ظاهر.

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
####  **يضيف Aspose.ThreeD.Formats. Secreet3dssaveoptions Class**
يحدد الإعدادات عند حفظ ملف 3DS غير ظاهر.

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
####  **يضيف Aspose.ThreeD.Formats.FBXSaveOptions Class**
يحدد الإعدادات عند حفظ ملف FBX.

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
####  **يضيف Aspose.ThreeD.Formats.ObjLoadOptions Class**
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

loadObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **يضيف Aspose.ThreeD.Formats.ObjSaveOptions Class**
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

saveObjOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

// serialize W component in model's vertex position

saveObjOpts.SerializeW = true;

// generate comments for each section

saveObjOpts.Verbose = true;

{{< /highlight >}}
####  **يضيف Aspose.ThreeD. Formaces. STLLoadOptions Class**
يحدد الإعدادات عند تحميل ملف STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLLoadOptions loadSTLOpts = new STLLoadOptions();

// flip the coordinate system.

loadSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **تضيف Aspose.ThreeD. Formes. STLSaveOptions Class**
يحدد الإعدادات عند حفظ ملف STL.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

STLSaveOptions saveSTLOpts = new STLSaveOptions();

// flip the coordinate system.

saveSTLOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

saveSTLOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **يضيف Aspose.ThreeD. Formaces. U3DLoadOptions Class**
إنه يحدد الإعدادات عند تحميل ملف U3D.

**C#**

{{< highlight "csharp" >}}

 // initialize an object

U3DLoadOptions loadU3DOpts = new U3DLoadOptions();

// flip the coordinate system.

loadU3DOpts.FlipCoordinateSystem = true;

// configure the look up paths to allow importer to find external dependencies.

loadU3DOpts.LookupPaths = new List<string>(new string[] { @"c:\temp\" });

{{< /highlight >}}
####  **يضيف Aspose.ThreeD.Formats.U3DSaveOptions Class**
يحدد الإعدادات عند حفظ ملف U3D.

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
###  **تضيف طرقًا إلى Aspose.ThreeD.Scene Class**
لقد قمنا بالحمل الزائد المفتوح وحفظ الطرق في فئة المشهد. يمكن للمطورين تمرير كائن دفق أو اسم ملف مباشر لاستيراد/تصدير ملف 3D باستخدام خيارات التحميل/التوفير المختلفة.

**C#**

{{< highlight "csharp" >}}

 public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options);

public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options);

public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options);

public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options);

{{< /highlight >}}
###  **إزالة خاصية filldummyindexary من Aspose.ThreeD. Fformes. FBXConfig Class**
Tلم يتم استخدام ممتلكاته.

**C#**

{{< highlight "csharp" >}}

 System.Nullable<Boolean> FillDummyIndexArray{ get;set;}

{{< /highlight >}}
###  **اكتشاف نوع ملف 3D**
يمكن لطريقة الكشف لفئة Aspose.ThreeD.FileFormat التعرف على نوع أي ملف 3D مدعوم.

**C#**

{{< highlight "csharp" >}}

 FileFormat inputFormat = FileFormat.Detect(@"C:\ThreeD\test06\colors.fbx");

Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
####  **يضيف طرق الكشف والتبني createloadtions و CreateSaveOptions في فئة Aspose.ThreeD.FileFormat**
بعد التعرف على نوع ملف 3D ، يمكن للمطورين إنشاء عمليات اعتماد وتحفظ كائنات لمهام التلاعب الإضافية.

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
###  **تضيف الخاصية المستبعدة إلى Aspose.ThreeD.Entity و Aspose.ThreeD.Node Classes**
يسمح It بإزالة كيان أثناء التصدير.

**C#**

{{< highlight "csharp" >}}

 bool Excluded{ get;set;}

{{< /highlight >}}
###  **يضيف Aspose.ThreeD. RenderState Class و Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/state**
Tانه يجعل الدول توفر المعلمات ل GPU لتمزيق مثلثات إلى بكسل.

{{% alert color="primary" %}} 

تغليف حالات تقديم الأجهزة ، يمكن العثور على المعلومات التفصيلية في وثائق [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml) ، [Dالمستقيم 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx) ، [Dالمستقيم 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) و [Vأولكان](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
###  **Adds ader hader APIs**
The Shader AIIs تحديد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU.
####  **يضيف فئة تجريدية Aspose.ThreeD.Render.ShaderSource والفئة الفرعية Aspose.ThreeD.Render.GLSLSource**
يخبر GLSLSource العارضات ، الشفرة المصدرية هي لغة تظليل OpenGL ، ويمكن تجميعها إلى Aspose.ThreeD.Render.ShaderProgram.
####  **تضيف Aspose.ThreeD.Render.ShaderException Class**
Tانه Sهادر الاستثناءات ذات الصلة ، وتستخدم أساسا في لغة شادر تجميع وربط المرحلة.
####  **تضيف Aspose.ThreeD.Render.ShaderProgram Class**
It هو برنامج shader مجمعة.
####  **أضف Aspose.ThreeD.Render.ShaderVariable Class**
It يحدد المتغيرات المستخدمة في شادر.
####  **يضيف فئة قائمة Aspose.ThreeD.Render.VariableSemantic**
يتم استخدامه لتحديد الدلالات الدلالية لمتغير التظليل ، Aspose. سيقوم المستعرض 3D بإعداد قيم التظليل المتغيرة تلقائيًا بناءً على الدلالات.
###  **Aدس ffer ffer ffer PIs**
Tهو المخازن المؤقتة توفير تعريف والبيانات من المثلثات.
####  **إضافة واجهة Aspose.ThreeD.Render. Ibuer**
It هو واجهة قاعدة ل InndexBuyee و ererertexBuvec.
####  **يضيف واجهات Aspose.ThreeD.Render. Iindexbover/ivertexbuer**
Hey يا مخازن الأجهزة الحالية لتخزين مؤشرات الهندسة.
####  **يضيف نموًا Aspose.ThreeD.Render.IndexDataType**
Tانه datatype من مؤشرات الهندسة.
###  **Adds ender ender ender Is**
####  **إضافة واجهة Aspose.ThreeD.Render.IRenderable**
An الكائن الذي يدعم تقديم يجب تنفيذ هذه الواجهة.
####  **تمت إضافة عدد Aspose.ThreeD. Ender. DrawOperation**
Tانه نوع بدائي لرسم.
####  **يضيف إنم Aspose.ThreeD. Reender. RenderQueueGroupId**
Aspose. يستخدم 3D API قائمة انتظار للتقديم لإدارة سير عمل التقديم ، ويتم استخدام هذا لإرسال عملية التقديم إلى قائمة انتظار محددة.
####  **تضيف Aspose.ThreeD. Rendersource Class**
Base class for bridging the Aspose.3D's model API to hardware resources, this is used by Aspose.3D internally, but exposed to unleash the full power of Aspose.3D rendering.
####  **تضيف Aspose.ThreeD. RenderableResource Class**
A Sub فئة من RenderResource ، ولكن التركيز على تقديم.
####  **تضيف Aspose.ThreeD. Forties. ManualEntity Class**
Tيجب على المستخدم استخدام هذه الفئة لتنفيذ كيانها الخاص الذي يدعم تقديم ، هذه الفئة تغليف تفاصيل تقديم العمليات وإدارة الموارد.
###  **تضيف طرق تثليث متعددة في فئة Aspose.ThreeD. Enties. PolygonModifier**
Mخام الزائد لتبسيط استخدام الوظيفة الأصلية.

**C#**

{{< highlight "csharp" >}}

 public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, IList<int[]> polygons);

public static int[][] Triangulate(IList<[Aspose.ThreeD.Utilities.Vector4> controlPoints, Int32[] polygon);

public static int[][] Triangulate(IList<Aspose.ThreeD.Utilities.Vector4> controlPoints);

{{< /highlight >}}
###  **يضيف createvertexbuer ، creatindexbuer ، CreateTextureUnit ، createrendestate و CreateShaderProgram أساليب في Aspose.ThreeD. RenderFactory Class**
**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Render.IVertexBuffer CreateVertexBuffer(Aspose.ThreeD.Utilities.VertexDeclaration declaration)

public Aspose.ThreeD.Render.IIndexBuffer CreateIndexBuffer()

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit()

public Aspose.ThreeD.Render.RenderState CreateRenderState()

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, IList<Aspose.ThreeD.Utilities.VertexField> inputFields)

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration)

{{< /highlight >}}
###  **تضيف طرق BindRenderState و drawinderstate و drawinded و drawing و submiderender في فئة Aspose.ThreeD. Renderer**
**C#**

{{< highlight "csharp" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Int32 first, Int32 count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, Int32 priority, Aspose.ThreeD.Render.IRenderable renderableTask)

{{< /highlight >}}
###  **تضيف خصائص RenderStage و Shader في فئة Aspose.ThreeD.Render**
**C#**

{{< highlight "csharp" >}}

 public RenderStage RenderStage { get; }

public Aspose.ThreeD.Render.ShaderProgram Shader{ get;set;}

{{< /highlight >}}
