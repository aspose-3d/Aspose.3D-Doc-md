---
title: Aspose.3D for .NET 19.12 tes elease tes otes
type: docs
weight: 10
url: /ar/net/aspose-3d-for-net-19-12-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 19.12.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|` `**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-590 |` ` Pفن المشهد فقدت عند تحويل ملف rvm إلى ملف glb|` `Bug|
|THREEDNET-597 |` `Problem تحميل الملف|` `Bug|
|THREEDNET-595 |` `Shadow خلق عند دمج مشهد|` `Bug|
## **Hangublic API و ackackward hangمتوافق مع hangمعلقة**
Tversion لديه اثنين من التغييرات الرئيسية API:

- Refactored نظام الرسوم المتحركة ، حتى نتمكن من حجز بعض الأسماء للاستخدام في المستقبل عندما سيتم دعم الأشكال CAD.
-إعادة تسمية نسخته**Curve**إلى**معادلة إيفريميرس**، و**Apping الربط الربط**إلى**Bإنديجو أونت**. سيتم إزالة واجهات obhe obsoleted من Aspose.3D for .NET 20.03. سوف توفر الطقوس التي تستخدم هذه الطبقات الاستبدال كبديل.
-While لا تزال الأسماء القديمة موجودة في 19.12 ، والرمز الذي يعتمد على هذه التغييرات يحتاج أقل أو حتى أي تغييرات (If يمكنك استخدام نوع المستنتج).
- تمت إعادة صياغة المنتج القديم OpenGL ، وأعاد النظر في المنتج لذلك يعمل بشكل أفضل مع سائق Vulkan الأساسي. تم تغيير واجهات مستوى ow مع الحفاظ على واجهات تقديم عالية المستوى سليمة.
-Tانه إعادة النظر في بائع لديه أداء تقديم أفضل ، مع المزيد من المرونة والتوسع.
-Tانه تقديم طريقة في**مشهد**الصف ليس له أي تغييرات. If يمكنك استخدام واجهة تقديم عالية المستوى ، لا تحتاج إلى تغيير أي شيء.
-Tأنه منخفض المستوى API لديه تغيير كسر ، قد تحتاج إلى الاتصال الدعم لترحيل التعليمات البرمجية.

Tما يلي معلومات مفصلة حول التغييرات العامة API في هذا الإصدار.

- الطبقة الملتزمة**Aspose.ThreeD. nimnimation. ururve**إلى**Aspose.ThreeD. nimnimation.**
- الطبقة الملتزمة**Aspose.ThreeD. nimnimation. urالربط الربط**إلى**Aspose.ThreeD. nimnimation. indindPoint**

يتم وضع علامة على الطرق/الخصائص ذات الصلة ll ll كما obsoleted وسيتم إزالتها في المستقبل ، ويتم توفير طرق/خصائص جديدة.
### **أعضاء Obsoleted في الفئة Aspose.ThreeD. nimnimation. nimnimationChannel**
- الفراغ العام ddddCurve (Aspose.ThreeD. nimnimation. منحنى urve)
- Ist Lالعام<Aspose.ThreeD.Animation.Curve>Ururves {get;}
#### **إعادة تعيين**
{{< highlight "java" >}}

 /// <summary>

/// Adds keyframe sequence to this channel

/// </summary>

/// <param name="sequence">The keyframe sequence to add.</param>

public void AddKeyframeSequence(Aspose.ThreeD.Animation.KeyframeSequence sequence)



/// <summary>

/// Gets all keyframe sequences inside this channel

/// </summary>

public IList<Aspose.ThreeD.Animation.KeyframeSequence> KeyframeSequences{ get;}

{{< /highlight >}}


### **أعضاء Obsoleted في الفئة Aspose.ThreeD. nimnimation. nimnimationNode**
{{< highlight "java" >}}

 public Aspose.ThreeD.Animation.CurveMapping FindCurveMapping(string name)

public Aspose.ThreeD.Animation.CurveMapping GetCurveMapping(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, string channelName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.CurveMapping CreateCurveMapping(Aspose.ThreeD.A3DObject obj, string propName)

public IList<Aspose.ThreeD.Animation.CurveMapping> CurveMappings{ get;}

{{< /highlight >}}
#### **إعادة تعيين**
{{< highlight "java" >}}

 /// <summary>

/// Finds the bind point by name.

/// </summary>

/// <returns>The bind point.</returns>

/// <param name="name">Bind point's name to find.</param>

public Aspose.ThreeD.Animation.BindPoint FindBindPoint(string name)

/// <summary>

/// Gets the animation bind point on given property.

/// </summary>

/// <returns>The bind point.</returns>

/// <param name="target">On which object to create the bind point.</param>

/// <param name="propName">The property's name.</param>

/// <param name="create">If set to <c>true</c> create the bind point if it's not existing.</param>

public Aspose.ThreeD.Animation.BindPoint GetBindPoint(Aspose.ThreeD.A3DObject target, string propName, bool create)

/// <summary>

/// Gets the keyframe sequence on given property and channel.

/// </summary>

/// <returns>The keyframe sequence.</returns>

/// <param name="target">On which instance to create the keyframe sequence.</param>

/// <param name="propName">The property's name.</param>

/// <param name="channelName">The channel name.</param>

/// <param name="create">If set to <c>true</c> create the animation sequence if it's not existing.</param>

public Aspose.ThreeD.Animation.KeyframeSequence GetKeyframeSequence(Aspose.ThreeD.A3DObject target, string propName, string channelName, bool create)

/// <summary>

/// Gets the keyframe sequence on given property and channel.

/// </summary>

/// <returns>The keyframe sequence.</returns>

/// <param name="target">On which instance to create the keyframe sequence.</param>

/// <param name="propName">The property's name.</param>

/// <param name="create">If set to <c>true</c> create the animation sequence if it's not existing.</param>

public Aspose.ThreeD.Animation.KeyframeSequence GetKeyframeSequence(Aspose.ThreeD.A3DObject target, string propName, bool create)

/// <summary>

/// Gets the keyframe sequence on given property and channel.

/// </summary>

/// <returns>The keyframe sequence.</returns>

/// <param name="target">On which instance to create the keyframe sequence.</param>

/// <param name="propName">The property's name.</param>

/// <param name="channelName">The channel name.</param>

/// <param name="create">If set to <c>true</c> create the animation sequence if it's not existing.</param>

public Aspose.ThreeD.Animation.BindPoint CreateBindPoint(Aspose.ThreeD.A3DObject obj, string propName)

/// <summary>

/// Gets the current property bind points

/// </summary>

public IList<Aspose.ThreeD.Animation.BindPoint> BindPoints{ get;}

{{< /highlight >}}
### **أعضاء Obsoleted في الفئة Aspose.ThreeD. roroperty**
- العامة Aspose.ThreeD. nimnimation. ururveMالربط etetCurveMالربط (Aspose.ThreeD. nimnimation. nimnimationNode أنيم ، bool إنشاء)
- العامة Aspose.ThreeD. nimnimation. ururve etetCurve (Aspose.ThreeD. nimnimation. nimnimationNode أنيم ، bool إنشاء)
#### **إعادة تعيين**
{{< highlight "java" >}}

 /// <summary>

/// Gets the property bind point on specified animation instance.

/// </summary>

/// <param name="anim">On which animation to create the bind point.</param>

/// <param name="create">Create the property bind point if it's not found.</param>

/// <returns>The property bind point on specified animation instance</returns>

public Aspose.ThreeD.Animation.BindPoint GetBindPoint(Aspose.ThreeD.Animation.AnimationNode anim, bool create)

/// <summary>

/// Gets the keyframe sequence on specified animation instance.

/// </summary>

/// <param name="anim">On which animation to create the keyframe sequence.</param>

/// <param name="create">Create the keyframe sequence if it's not found.</param>

/// <returns>The keyframe sequence on specified animation instance</returns>

public Aspose.ThreeD.Animation.KeyframeSequence GetKeyframeSequence(Aspose.ThreeD.Animation.AnimationNode anim, bool create)

{{< /highlight >}}
### **Mالجمر Added**
` ` أعضاء dded إلى الفئة**Aspose.ThreeD. nntities. VertexEleالقابل UserData**

{{< highlight "java" >}}

 /// <summary>

/// The user data attached in this element

/// </summary>

public Dictionary<string, object> Data{ get;}

{{< /highlight >}}

أعضاء Added إلى الصف**Aspose.ThreeD.**

{{< highlight "java" >}}

 /// <summary>

/// Create the descriptor set for specified shader program.

/// </summary>

/// <param name="shader">The shader program</param>

/// <returns>A new descriptor set instance</returns>

public Aspose.ThreeD.Render.IDescriptorSet CreateDescriptorSet(Aspose.ThreeD.Render.ShaderProgram shader)

/// <summary>

/// Create a <see cref="ShaderProgram"/> object

/// </summary>

/// <param name="shaderSource">The source code of the shader</param>

/// <returns></returns>

public Aspose.ThreeD.Render.ShaderProgram CreateShaderProgram(Aspose.ThreeD.Render.ShaderSource shaderSource)

/// <summary>

/// Create a preconfigured graphics pipeline with preconfigured shader/render state/vertex declaration and draw operations.

/// </summary>

/// <param name="shader">The shader used in the rendering</param>

/// <param name="renderState">The render state used in the rendering</param>

/// <param name="vertexDeclaration">The vertex declaration of input vertex data</param>

/// <param name="drawOperation">Draw operation</param>

/// <returns>A new pipeline instance</returns>

public Aspose.ThreeD.Render.IPipeline CreatePipeline(Aspose.ThreeD.Render.ShaderProgram shader, Aspose.ThreeD.Render.RenderState renderState, Aspose.ThreeD.Utilities.VertexDeclaration vertexDeclaration, Aspose.ThreeD.Render.DrawOperation drawOperation)

/// <summary>

/// Create a new uniform buffer in GPU side with preallocated size.

/// </summary>

/// <param name="size">The size of the uniform buffer</param>

/// <returns>The uniform buffer instance</returns>

public Aspose.ThreeD.Render.IBuffer CreateUniformBuffer(int size)

{{< /highlight >}}

أعضاء Added إلى الصف**Aspose.ThreeD. Rاندر. enenderer**

{{< highlight "java" >}}

 /// <summary>

/// Register the entity renderer for specified entity

/// </summary>

/// <param name="renderer"></param>

public void RegisterEntityRenderer(Aspose.ThreeD.Render.EntityRenderer renderer)

/// <summary>

/// Gets the command list for specified render queue

/// </summary>

/// <param name="queueGroup"></param>

/// <returns></returns>

public Aspose.ThreeD.Render.ICommandList GetCommandList(Aspose.ThreeD.Render.RenderQueueGroupId queueGroup)

/// <summary>

/// Gets or sets the fallback entity renderer when the entity has no special renderer defined.

/// </summary>

Aspose.ThreeD.Render.EntityRenderer FallbackEntityRenderer{ get;set;}

/// <summary>

/// Access to the internal variables used for rendering

/// </summary>

Aspose.ThreeD.Render.RendererVariableManager Variables{ get;}

{{< /highlight >}}


### **Mالجمر emoالرموز التعبيرية**
Rفئة عاطفية**Aspose.ThreeD-مدير الصندوق**

Tانه قاعدة فئة من الحد الأدنى تجعل مهمة في العمارة تقديم القديمة. Tانه بائع جديد يفصل نموذج الكائن الذي صمم لقراءة الملف/الكتابة وتنفيذ تقديم ، وبالتالي فإن RenderableResource لم تعد هناك حاجة.

{{< highlight "java" >}}

 public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, IList<VertexField> inputFields);

public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState CreateRenderState();

{{< /highlight >}}

أعضاء عاطفية غير مسبوقة من الطبقة**Aspose.ThreeD. Rاندر. enenderer**

أعضاء إزالة ese hese هي تقديم مستوى منخفض ذات الصلة ، في 19.12 سوف يكون ist ntityRenderer و ist omommanList مسؤولا عن تنفيذ التقديم.

{{< highlight "java" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, int first, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, int priority, Aspose.ThreeD.Node node, Aspose.ThreeD.Render.IRenderable renderableTask)

public Aspose.ThreeD.Render.Renderer CurrentContext{ get;}

{{< /highlight >}}

- Rالمشاعر enum**Aspose.ThreeD.**
-بعد ذلك ، لن يتمكن المُؤجر في 19.12 من إدارة متغير التظليل ، بدلاً من ذلك ، سيوفر كل تنفيذ لمؤجر الكيان البيانات المطلوبة للشادر يدويًا من خلال دفع المخزن المؤقت المستمر أو الموحد ، مما يجعل المستأجر أكثر كفاءة وأكثر بساطة.
- عضو مثير للاهتمام من**Aspose.ThreeD. ender اندر. hadhaderVariable**
-العامة ariariableSالمنبثقة eman{ get;}
- أعضاء عاطفية غير مسبوقة من الطبقة**Aspose.ThreeD. Rاندر. hadhaderProgram**
-العامة Iist ist<Aspose.ThreeD.Render.ShaderVariable>Ariariables {get;set;}
- Rفئة عاطفية**Aspose.ThreeD-مدير الصندوق**
-Tانه قاعدة فئة من الحد الأدنى يجعل المهمة في العمارة تقديم القديمة. Tانه بائع جديد يفصل نموذج الكائن الذي صمم لقراءة الملف/الكتابة وتنفيذ تقديم ، وبالتالي فإن RenderableResource لم تعد هناك حاجة.
### **Classes Added**
- فئة ded dded**Aspose.ThreeD. ender اندر. nntityRenderer**
-Subclass هذا لتوفير تقديم التنفيذ للكيانات المحددة.
- فئة ded dded**Aspose.ThreeD. Rأندر.**
-Tانه دون تصنيف EntityRenderer يستخدم ist ommanList لترميز التعليمات لجعل الكيان.
- فئة ded dded**Aspose.ThreeD. ender اندر. IesescriptorSet**
-Tهو مجموعة الوصف هو مجموعة من الوصفات ، وصفي يمكن أن يكون عازلة موحدة ، وحدة الملمس أو غيرها من الموارد الجانبية GPU. If كيانات متعددة تشارك نفس خط أنابيب الرسومات ولكن مع مواد مختلفة وغيرها من البيانات ، فإنها يمكن أن تستخدم IesescriptorSet لتوفير البيانات لكل كيان.
- فئة ded dded**Aspose.ThreeD. ender اندر. esescriptorSetUpdater**
-لا يوفر he he esescriptorSet واجهة لتغيير وصفاتها المحدودة ، مطلوب pdater escriptorSetUetdatلارتكاب تحديثات متعددة ل GU U.
- فئة ded dded**Aspose.ThreeD. Rاندر. enendererVariableManager**
-When تقديم كيان يدويا ، وعادة ما تكون هناك حاجة إلى بعض المتغيرات الداخلية مثل عرض/مصفوفة الإسقاط ، ويمكن العثور على هذه في RendererVariableManager.
- فئة ded dded**Aspose.ThreeD. ender ender. SPource ource ource ource**
-Hen hen إنشاء برنامج شادر على سبيل المثال ، هناك حاجة إلى مصدر SPIR-V ، SPIR-V هو رمز بايت ل Vulkan تجميعها من GLL L أو غيرها من اللغات شادر.
- فئة ded dded**Aspose.ThreeD. تيلز tili. تيلز Iti**
-Rorovided بعض طرق التمديد لكتابة مصفوفة/ناقلات إلى ritinaryWطقوس.
- فئة ded dded**Aspose.ThreeD. ender اندر. Iipipبلون**
-Tانه تسلسل مسبقا من العمليات لرسم في الجانب GPU ، عندما يتم إنشاء خط أنابيب الرسومات ، فإن سائق Gunderlying underlying الأساسي لن تحتاج إلى إعادة التحقق من حالة تقديم/ظلال إعادة تجميع في مكالمة رسم ، والتي يمكن أن تحسن كثيرا من أداء تقديم.
### **Classes الرموز التعبيرية**
- Rفئة عاطفية**Aspose.ThreeD-مدير الصندوق**
-Tانه قاعدة فئة من الحد الأدنى يجعل المهمة في العمارة تقديم القديمة. Tانه بائع جديد يفصل نموذج الكائن الذي صمم لقراءة الملف/الكتابة وتنفيذ تقديم ، وبالتالي فإن RenderableResource لم تعد هناك حاجة.


