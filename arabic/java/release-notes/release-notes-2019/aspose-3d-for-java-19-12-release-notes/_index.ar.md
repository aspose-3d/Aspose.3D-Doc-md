---
title: Aspose.3D for Java 19.12 tes elease tes otes
type: docs
weight: 10
url: /ar/java/aspose-3d-for-java-19-12-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 19.12.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|` `**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-590 |` ` Pفن المشهد فقدت عند تحويل ملف rvm إلى ملف glb|` `Bug|
|THREEDNET-597 |` `Problem تحميل الملف|` `Bug|
|THREEDNET-595 |` ` hadow hadow التي تم إنشاؤها عند دمج المشهد|` `Bug|
## **Hangublic API و ackackward hangمتوافق مع hangمعلقة**
Tversion لديه اثنين من التغييرات الرئيسية API:

- Refactored نظام الرسوم المتحركة ، حتى نتمكن من حجز بعض الأسماء للاستخدام في المستقبل عندما سيتم دعم الأشكال CAD.
-إعادة تسمية نسخته**Curve**إلى**معادلة إيفريميرس**، و**Apping الربط الربط**إلى**Bإنديجو أونت**. سيتم إزالة واجهات obhe obsoleted من Aspose.3D for .NET 20.03. سوف توفر الطقوس التي تستخدم هذه الطبقات الاستبدال كبديل.
-While لا تزال الأسماء القديمة موجودة في 19.12 ، والرمز الذي يعتمد على هذه التغييرات تحتاج أقل أو حتى أي تغييرات (If يمكنك استخدام نوع المستنتج).
- تمت إعادة صياغة المنتج القديم OpenGL ، وأعاد النظر في المنتج لذلك يعمل بشكل أفضل مع سائق Vulkan الأساسي. تم تغيير واجهات مستوى ow مع الحفاظ على واجهات تقديم عالية المستوى سليمة.
-Tانه إعادة النظر في العارض لديه أفضل تقديم الأداء ، مع المزيد من المرونة والتوسع.
-Tانه تقديم طريقة في**مشهد**الصف ليس له أي تغييرات. If يمكنك استخدام واجهة تقديم عالية المستوى ، لا تحتاج إلى تغيير أي شيء.
-Tأنه منخفض المستوى API لديه تغيير كسر ، قد تحتاج إلى الاتصال الدعم لترحيل التعليمات البرمجية.

Tما يلي معلومات مفصلة حول التغييرات العامة API في هذا الإصدار.

- الطبقة الملتزمة**كوم. أسبوس. ثريد. منحنى**إلى**كوم. أسبوس. ثريد.**
- الطبقة الملتزمة**Com. aspose.threed. urالربط الربط**إلى**كوم. أسبوس. ثريدن.**

يتم وضع علامة على الطرق/الخصائص ذات الصلة ll ll كما obsoleted وسيتم إزالتها في المستقبل ، ويتم توفير طرق/خصائص جديدة.
### **أعضاء Obsoleted في الفئة com.aspose.threed. nimnimationCهاننيل**
{{< highlight "java" >}}

 public void AddCurve(com.aspose.threed.Curve curve)

public IList<com.aspose.threed.Curve> getCurves()

{{< /highlight >}}
#### **إعادة تعيين**
{{< highlight "java" >}}

 /**

     * Adds keyframe sequence to this channel

     * @param sequence The keyframe sequence to add.

     */

    public void addKeyframeSequence(KeyframeSequence sequence);

    /**

     * Gets all keyframe sequences inside this channel

     */

    public List<KeyframeSequence> getKeyframeSequences();

{{< /highlight >}}
### **أعضاء Obsoleted في الفئة com.aspose.threed. nimnimationNode**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping findCurveMapping(String name)

public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, String channelName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.CurveMapping createCurveMapping(com.aspose.threed.A3DObject obj, String propName)

public IList<com.aspose.threed.CurveMapping> getCurveMappings()

{{< /highlight >}}
#### **إعادة تعيين**
{{< highlight "java" >}}

     /**

     * Finds the bind point by name.

     * @param name Bind point's name to find.

     * @return The bind point.

     */

    public BindPoint findBindPoint(String name);

    /**

     * Gets the animation bind point on given property.

     * @param target On which object to create the bind point.

     * @param propName The property's name.

     * @param create If set to {@code true} create the bind point if it's not existing.

     * @return The bind point.

     */

    public BindPoint getBindPoint(A3DObject target, String propName, boolean create);

    /**

     * Gets the keyframe sequence on given property and channel.

     * @param target On which instance to create the keyframe sequence.

     * @param propName The property's name.

     * @param channelName The channel name.

     * @param create If set to {@code true} create the animation sequence if it's not existing.

     * @return The keyframe sequence.

     */

    public KeyframeSequence getKeyframeSequence(A3DObject target, String propName, String channelName, boolean create);

    /**

     * Gets the keyframe sequence on given property.

     * @param target On which instance to create the keyframe sequence.

     * @param propName The property's name.

     * @param create If set to {@code true}, create the sequence if it's not existing.

     * @return The keyframe sequence.

     */

    public KeyframeSequence getKeyframeSequence(A3DObject target, String propName, boolean create);

    /**

     * Creates a BindPoint based on the property data type.

     * @param obj Object.

     * @param propName Property name.

     * @return The bind point instance or null if the property is not defined.

     */

    public BindPoint createBindPoint(A3DObject obj, String propName)

    /**

     * Gets the current property bind points

     */

    public List<BindPoint> getBindPoints();

{{< /highlight >}}
### **أعضاء Obsoleted في فئة com. asshape. threed. roroperty**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.AnimationNode anim, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.AnimationNode anim, boolean create)

{{< /highlight >}}
#### **إعادة تعيين**
{{< highlight "java" >}}

 /**

\* Gets the property bind point on specified animation instance.

\* @param anim On which animation to create the bind point.

\* @param create Create the property bind point if it's not found.

\* @return The property bind point on specified animation instance

*/

public BindPoint getBindPoint(AnimationNode anim, boolean create);

/**

\* Gets the keyframe sequence on specified animation instance.

\* @param anim On which animation to create the keyframe sequence.

\* @param create Create the keyframe sequence if it's not found.

\* @return The keyframe sequence on specified animation instance

*/

public KeyframeSequence getKeyframeSequence(AnimationNode anim, boolean create);

{{< /highlight >}}
### **Mالجمر Added**
أعضاء Added إلى الصف**كوم. أسبوس. ثريد.**

{{< highlight "java" >}}

 /**

\* The user data attached in this element

*/

public Map<String, Object> getData();

{{< /highlight >}}

أعضاء Added إلى الصف**كوم. أسبوس. ثريد.**



{{< highlight "java" >}}

 /**

\* Create the descriptor set for specified shader program.

\* @param shader The shader program

\* @return A new descriptor set instance

*/

public IDescriptorSet createDescriptorSet(ShaderProgram shader);

/**

\* Create a {@link com.aspose.threed.ShaderProgram} object

\* @param shaderSource The source code of the shader

*/

public ShaderProgram createShaderProgram(ShaderSource shaderSource);

/**

\* Create a preconfigured graphics pipeline with preconfigured shader/render state/vertex declaration and draw operations.

\* @param shader The shader used in the rendering

\* @param renderState The render state used in the rendering

\* @param vertexDeclaration The vertex declaration of input vertex data

\* @param drawOperation Draw operation

\* @return A new pipeline instance

*/

public IPipeline createPipeline(ShaderProgram shader, RenderState renderState, VertexDeclaration vertexDeclaration, DrawOperation drawOperation);

/**

\* Create a new uniform buffer in GPU side with preallocated size.

\* @param size The size of the uniform buffer

\* @return The uniform buffer instance

*/

public IBuffer createUniformBuffer(int size);

{{< /highlight >}}

أعضاء Added إلى الصف**كوم. أسبوس. ثريد.**



{{< highlight "java" >}}

     /**

     * Register the entity renderer for specified entity

     * @param renderer 

     */

    public void registerEntityRenderer(EntityRenderer renderer);

    /**

     * Gets the command list for specified render queue

     * @param queueGroup 

     */

    public ICommandList getCommandList(RenderQueueGroupId queueGroup);

    /**

     * Gets the fallback entity renderer when the entity has no special renderer defined.

     */

    public EntityRenderer getFallbackEntityRenderer();

    /**

     * Sets the fallback entity renderer when the entity has no special renderer defined.

     * @param value New value

     */

    public void setFallbackEntityRenderer(EntityRenderer value);

    /**

     * Access to the internal variables used for rendering

     */

    public RendererVariableManager getVariables();

{{< /highlight >}}
### **Mالجمر emoالرموز التعبيرية**
أعضاء عاطفية غير مسبوقة من الطبقة**كوم. أسبوس. ثريد.**

` `Tانه renderer في 19.12 سوف نستنتج تخطيط الذاكرة vertex' من فيرتكس شادر تلقائيا ، لا حاجة لتوفير تفاصيل تخطيط الذاكرة vertex' يدويا. In 19.12 هناك جديد createShaderProgram المقدمة التي تحتاج فقط حجة واحدة. Tتم إزالة createRenderState ، ولكن تم إضافة منشئ RenderState ، يمكنك إنشاء enenderState باستخدام منشئ الافتراضي.



{{< highlight "java" >}}

 public ShaderProgram createShaderProgram(ShaderSource shaderSource, List<VertexField> inputFields);

public ShaderProgram createShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState createRenderState();

{{< /highlight >}}

أعضاء عاطفية غير مسبوقة من الطبقة**كوم. أسبوس. ثريد. Rاندر. enenderer**

أعضاء إزالة ese hese هي تقديم مستوى منخفض ذات الصلة ، في 19.12 سوف يكون ist ntityRenderer و ist omommanList مسؤولا عن تنفيذ التقديم.

{{< highlight "java" >}}

 public void bindRenderState(com.aspose.threed.RenderState renderState)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer, int count)

public void Draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, int first, int count)

public void draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer)

public void submitRenderTask(com.aspose.threed.RenderQueueGroupId groupId, int priority, com.aspose.threed.Node node, com.aspose.threed.IRenderable renderableTask)

{{< /highlight >}}



- Rالمشاعر enum**كوم. أسبوس. ثريد.**
-بعد ذلك ، لن يتمكن المُؤجر في 19.12 من إدارة متغير التظليل ، بدلاً من ذلك ، سيوفر كل تنفيذ لمؤجر الكيان البيانات المطلوبة للشادر يدويًا من خلال دفع المخزن المؤقت المستمر أو الموحد ، مما يجعل المستأجر أكثر كفاءة وأكثر بساطة.
- عضو مثير للاهتمام من**كوم. أسبوس. ثريد.**
-العامة ariariableSالمنبثقة eman{ get;}
- أعضاء عاطفية غير مسبوقة من الطبقة**كوم. أسبوس. ثريد.**
-العامة Iist ist<Aspose.ThreeD.Render.ShaderVariable>Ariariables {get;set;}
### **Classes Added**
- فئة ded dded**Com. aspose.threed. nntityRenderer**
-Subclass هذا لتوفير تقديم التنفيذ للكيانات المحددة.
- فئة ded dded**كوم. أسبوس. ثريد.**
-Tانه دون تصنيف EntityRenderer يستخدم ist ommanList لترميز التعليمات لجعل الكيان.
- فئة ded dded**Com. aspose.threed. esesescriptorSet**
-Tهو مجموعة الوصف هو مجموعة من الوصفات ، وصفي يمكن أن يكون عازلة موحدة ، وحدة الملمس أو غيرها من الموارد الجانبية GPU. If كيانات متعددة تشارك نفس خط أنابيب الرسومات ولكن مع مواد مختلفة وغيرها من البيانات ، فإنها يمكن أن تستخدم IesescriptorSet لتوفير البيانات لكل كيان.
- فئة ded dded**Com. aspose.threed. esescriptorSetUpdater**
-لا يوفر he he esescriptorSet واجهة لتغيير وصفاتها المحدودة ، مطلوب pdater escriptorSetUetdatلارتكاب تحديثات متعددة ل GU U.
- فئة ded dded**كوم. أسبوس. ثريد.**
-When تقديم كيان يدويا ، وعادة ما تكون هناك حاجة إلى بعض المتغيرات الداخلية مثل عرض/مصفوفة الإسقاط ، ويمكن العثور على هذه في RendererVariableManager.
- فئة ded dded**Com. aspose.threed. SPRource ource ource**
-Hen hen إنشاء برنامج شادر على سبيل المثال ، هناك حاجة إلى مصدر SPIR-V ، SPIR-V هو رمز بايت ل Vulkan تجميعها من GLL L أو غيرها من اللغات شادر.
- فئة ded dded**كوم. أسبوس. ثريد.**
-Rorovided بعض طرق التمديد لكتابة مصفوفة/ناقلات إلى ritinaryWطقوس.
- فئة ded dded**كوم. أسبوس. ثريد.**
-Tانه تسلسل مسبقا من العمليات لرسم في الجانب GPU ، عندما يتم إنشاء خط أنابيب الرسومات ، فإن سائق Gunderlying underlying الأساسي لن تحتاج إلى إعادة التحقق من حالة تقديم/ظلال إعادة تجميع في مكالمة رسم ، والتي يمكن أن تحسن كثيرا من أداء تقديم.
### **Classes الرموز التعبيرية**
- Rفئة عاطفية**Aspose.ThreeD-مدير الصندوق**
-Tانه قاعدة فئة من الحد الأدنى يجعل المهمة في العمارة تقديم القديمة. Tانه بائع جديد يفصل نموذج الكائن الذي صمم لقراءة الملف/الكتابة وتنفيذ تقديم ، وبالتالي فإن RenderableResource لم تعد هناك حاجة.
