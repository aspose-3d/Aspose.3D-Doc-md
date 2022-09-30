---
title: Aspose.3D for Java 19,12 Utgivning
type: docs
weight: 10
url: /sv/java/aspose-3d-for-java-19-12-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for Java 19.12.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-590 |` `En del av scenen förlorade när du konverterar en rvm-fil till glb-filen|` `Bug|
|THREEDNET-597 |` `Problemlastningsfil|` `Bug|
|THREEDNET-595 |` `Skyg skapad när scenen slås samman.|` `Bug|
## **Offentlig API och bakåtkompatibla förändringar**
Denna version har två större ändringar API:

- Refactorerad animationssystemet, så att vi kan reservera några namn för framtida användning när CAD format stöds.
- Den här versionen bytt namn**Kurva**Till följd**NyckelramSequens**, Och**Kurvbildning**Till följd**BindPointName**. De föråldrade gränssnitten kommer att tas bort från Aspose.3D for .NET 20.03. Metoder som använder dessa klasser kommer att ge ersättning som ett alternativ.
- Medan de gamla namnen fortfarande finns i 19.12, koden som beror på dessa ändringar behöver mindre eller till och med inga ändringar (Om du använder typ infer).
- Ta bort arven OpenGL renderare, och tillverkade återgivaren så att den fungerar bäst med den underliggande Vulkan föraren. Gränssnitt på låg nivå har ändrats samtidigt som de hög nivå renderingsgränssnitten hålls intakta.
- Den refaktored renderare har bättre renderingsprestanda, med mer flexibilitet och extensibilitet.
- Reservmetoden i**Scen**Klassen har inga förändringar. Om du använder ett gränssnitt på hög nivå behöver du inte ändra någonting.
- Den låga nivån API har en brytande förändring, du kan behöva kontakta stöd för kodmigration.

Nedanstående är detaljerad information om allmänheten API ändringar i denna version.

- Byt ut klass**Com.aspose.**Till följd**Com.aspose.**
- Byt ut klass**Com.aspose.3**Till följd**Com.aspose.3.BindPoint.**

Alla relaterade metoder/egenskaper är markerade som föråldrade och kommer att tas bort i framtiden och nya metoder/egenskaper tillhandahålls.
### **Föråldrade medlemmar i klassen com.aspose.3reed.AnimationChannel**
{{< highlight "java" >}}

 public void AddCurve(com.aspose.threed.Curve curve)

public IList<com.aspose.threed.Curve> getCurves()

{{< /highlight >}}
#### **Ersättningar**
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
### **Föråldrade medlemmar i klass com.aspose.3reed.AnimationNode.**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping findCurveMapping(String name)

public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, String channelName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.CurveMapping createCurveMapping(com.aspose.threed.A3DObject obj, String propName)

public IList<com.aspose.threed.CurveMapping> getCurveMappings()

{{< /highlight >}}
#### **Ersättningar**
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
### **Föråldrade medlemmar i klass com.aspose.3reed.Property**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.AnimationNode anim, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.AnimationNode anim, boolean create)

{{< /highlight >}}
#### **Ersättningar**
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
### **Ledamöter**
Medlemmar till klass**Com.aspose. Threed. VertexElementUserData**

{{< highlight "java" >}}

 /**

\* The user data attached in this element

*/

public Map<String, Object> getData();

{{< /highlight >}}

Medlemmar till klass**Com.aspose.3.RenderFactory**



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

Medlemmar till klass**Com.aspose.**



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
### **Ledamöter**
Avlägsnade medlemmar från klass**Com.aspose.3.RenderFactory**

` `Den renderare i 19.12 kommer att dra slutpunkten "minnen layout från vertex shader automatiskt, inget behov av att manuellt tillhandahålla vertex minnes layout detaljer. I 19.12 finns det nytt skapaShaderProgram som bara behöver ett argument. Den createRenderState togs bort, men konstruktören av RenderState lades till, du kan skapa RenderState med sin standardkonstruktör.



{{< highlight "java" >}}

 public ShaderProgram createShaderProgram(ShaderSource shaderSource, List<VertexField> inputFields);

public ShaderProgram createShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState createRenderState();

{{< /highlight >}}

Avlägsnade medlemmar från klass**Com.aspose.**

Dessa borttagna medlemmar är låg nivå rendering relaterade, Under 19.12 kommer EntityRenderer och ICommandList att ansvara för implementeringen.

{{< highlight "java" >}}

 public void bindRenderState(com.aspose.threed.RenderState renderState)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer, int count)

public void Draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, int first, int count)

public void draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer)

public void submitRenderTask(com.aspose.threed.RenderQueueGroupId groupId, int priority, com.aspose.threed.Node node, com.aspose.threed.IRenderable renderableTask)

{{< /highlight >}}



- Borttagen enum**Com.aspose.**
- Renderaren i 19.12 kommer inte längre att hantera skuggarvariabeln, istället, Varje enhet redigerar implementering kommer manuellt att tillhandahålla de uppgifter som behövs till skuggaren genom push konstant eller enhetlig buffert. detta gör återgivaren effektivare och enklare.
- Avlägsnad medlem från**Com.aspose. Threed. Shadarvariabler**
- Offentlig variabelSemantic Semantic { get;}
- Avlägsnade medlemmar från klass**Com.aspose. 3.**
- Public IList<Aspose.ThreeD.Render.ShaderVariable>Variabler{ get;set;}
### **Klasser**
- Tillagd klass**Com.aspose.3.EntityRenderer**
- Underklass detta för att tillhandahålla rendering implementering för angivna enheter.
- Tillagd klass**Com.aspose.treed.ICommandlista**
- Den underklassade EntityRenderer använder ICommandList för att koda instruktionerna för att visa enheten.
- Tillagd klass**Com.aspose. Threed.IDescriptorSetComment**
- Deskriptorn är en uppsättning deskriptorer, en deskriptor kan vara en enhetlig buffert, strukturenhet eller andra GPU-sidaresurser. Om flera enheter delar samma grafiska rörledning men med olika texturer och andra data, de kan använda IDescriptorSet för att tillhandahålla per enhetsdata.
- Tillagd klass**Com.aspose.3**
- IDescriptorSet tillhandahåller inte ett gränssnitt för att ändra dess begränsade deskriptorer, en DescriptorSetUpdater krävs för att skicka flera uppdateringar till GPU.
- Tillagd klass**Com.aspose. 3.**
- Vid återgivning av en enhet manuellt behövs vanligtvis vissa interna variabler som visning/projection matris, dessa finns på RendererVariableManager.
- Tillagd klass**Com.aspose.3.**
- När du skapar en shader programinstans behövs SPIR-V-källan, SPIR-V är byte-kod för Vulkan kompilerad från GLSL eller andra språk.
- Tillagd klass**Com.aspose.3reed.IOUtils**
- Tillhandahöll vissa förlängningsmetoder för att skriva matris/vektor till BinaryWriter.
- Tillagd klass**Com.aspose.**
- Den förbakade sekvensen av verksamheter för att dra i GPU sidan, när grafikrörledningen skapas, den underliggande GPU-drivrutinen behöver inte förlänga renderingstillstånd/recompile shaders i ett dragsamtal, som avsevärt kan förbättra renderingsprestandan.
### **Avlägsnade klasser**
- Ta bort klass**Aspose.ThreeD.Render.Renderbar ressource.**
- Basklassen av den minsta renderar uppgiften i gamla rendering arkitektur. Den nya renderaren separerar objektmodellen som är utformad för filläsning/skrivning och implementering av rendering, Så RenderableResource behövs inte längre.
