---
title: Aspose.3D for .NET 19,12 Utgivning
type: docs
weight: 10
url: /sv/net/aspose-3d-for-net-19-12-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for .NET 19.12.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-590 |` `En del av scenen förlorade när du konverterar en rvm-fil till glb-filen|` `Bug|
|THREEDNET-597 |` `Problemlastningsfil|` `Bug|
|THREEDNET-595 |` `Shadow skapad när en scen slås samman.|` `Bug|
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

- Byt ut klass**Aspose.ThreeD.Animation.**Till följd**Aspose.ThreeD.Animation.**
- Byt ut klass**Aspose.ThreeD.Animation.**Till följd**Aspose.ThreeD.Animation.BindPoint.**

Alla relaterade metoder/egenskaper är markerade som föråldrade och kommer att tas bort i framtiden och nya metoder/egenskaper tillhandahålls.
### **Föråldrade medlemmar i klass Aspose.ThreeD.AnimationChannel**
- Offentligt tomrum AddCurve(Aspose.ThreeD.Animation.Curve kurva)
- Public IList<Aspose.ThreeD.Animation.Curve>Kurvor{ get;}
#### **Ersättningar**
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


### **Föråldrade medlemmar i klass Aspose.ThreeD.AnimationNode.**
{{< highlight "java" >}}

 public Aspose.ThreeD.Animation.CurveMapping FindCurveMapping(string name)

public Aspose.ThreeD.Animation.CurveMapping GetCurveMapping(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, string channelName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.CurveMapping CreateCurveMapping(Aspose.ThreeD.A3DObject obj, string propName)

public IList<Aspose.ThreeD.Animation.CurveMapping> CurveMappings{ get;}

{{< /highlight >}}
#### **Ersättningar**
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
### **Föråldrade medlemmar i klass Aspose.ThreeD**
- Offentlig Aspose.ThreeD. Animation. Tryckkartbildning för att trycka kartläggning(Aspose.ThreeD. Animation. AnimationNode anim, bool create)
- Offentlig Aspose.ThreeD. Animation. Curve GetCurve(Aspose.ThreeD. Animation. AnimationNode anim, bool create)
#### **Ersättningar**
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
### **Ledamöter**
` `Medlemmar i klass**Aspose.ThreeD.Enheter.VertexElementUserData.**

{{< highlight "java" >}}

 /// <summary>

/// The user data attached in this element

/// </summary>

public Dictionary<string, object> Data{ get;}

{{< /highlight >}}

Medlemmar till klass**Aspose.ThreeD.Render.RenderFactory**

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

Medlemmar till klass**Aspose.ThreeD.Render.Renderer**

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


### **Ledamöter**
Ta bort klass**Aspose.ThreeD.Render.Renderbar ressource.**

Basklassen för den minsta renderingsuppgiften i gammal renderingsarkitektur. Den nya renderaren separerar objektmodellen som är utformad för filläsning/skrivning och implementering av rendering, Så RenderableResource behövs inte längre.

{{< highlight "java" >}}

 public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, IList<VertexField> inputFields);

public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState CreateRenderState();

{{< /highlight >}}

Avlägsnade medlemmar från klass**Aspose.ThreeD.Render.Renderer**

Dessa borttagna medlemmar är låg nivå rendering relaterade, Under 19.12 kommer EntityRenderer och ICommandList att ansvara för implementeringen.

{{< highlight "java" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, int first, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, int priority, Aspose.ThreeD.Node node, Aspose.ThreeD.Render.IRenderable renderableTask)

public Aspose.ThreeD.Render.Renderer CurrentContext{ get;}

{{< /highlight >}}

- Borttagen enum**Aspose.ThreeD.**
- Renderaren i 19.12 kommer inte längre att hantera skuggarvariabeln, istället, Varje enhet redigerar implementering kommer manuellt att tillhandahålla de uppgifter som behövs till skuggaren genom push konstant eller enhetlig buffert. detta gör återgivaren effektivare och enklare.
- Avlägsnad medlem från**Aspose.ThreeD.**
- Offentlig variabelSemantic Semantic { get;}
- Avlägsnade medlemmar från klass**Aspose.ThreeD.Render.ShaderProgram.**
- Public IList<Aspose.ThreeD.Render.ShaderVariable>Variabler{ get;set;}
- Ta bort klass**Aspose.ThreeD.Render.Renderbar ressource.**
- Basklassen av den minsta renderar uppgiften i gamla rendering arkitektur. Den nya renderaren separerar objektmodellen som är utformad för filläsning/skrivning och implementering av rendering, Så RenderableResource behövs inte längre.
### **Klasser**
- Tillagd klass**Aspose.ThreeD.Render.EntityRenderer**
- Underklass detta för att tillhandahålla rendering implementering för angivna enheter.
- Tillagd klass**Aspose.ThreeD.Render.ICommandlista**
- Den underklassade EntityRenderer använder ICommandList för att koda instruktionerna för att visa enheten.
- Tillagd klass**Aspose.ThreeD.Render.IDescriptorSetName**
- Deskriptorn är en uppsättning deskriptorer, en deskriptor kan vara en enhetlig buffert, strukturenhet eller andra GPU-sidaresurser. Om flera enheter delar samma grafiska rörledning men med olika texturer och andra data, de kan använda IDescriptorSet för att tillhandahålla per enhetsdata.
- Tillagd klass**Aspose.ThreeD.Render.DescriptorSetUpdater**
- IDescriptorSet tillhandahåller inte ett gränssnitt för att ändra dess begränsade deskriptorer, en DescriptorSetUpdater krävs för att skicka flera uppdateringar till GPU.
- Tillagd klass**Aspose.ThreeD.Render.Rendervariabelhanterare**
- Vid återgivning av en enhet manuellt behövs vanligtvis vissa interna variabler som visning/projection matris, dessa finns på RendererVariableManager.
- Tillagd klass**Aspose.ThreeD.Render.SPIRVSource**
- När du skapar en shader programinstans behövs SPIR-V-källan, SPIR-V är byte-kod för Vulkan kompilerad från GLSL eller andra språk.
- Tillagd klass**Aspose.ThreeD.**
- Tillhandahöll vissa förlängningsmetoder för att skriva matris/vektor till BinaryWriter.
- Tillagd klass**Aspose.ThreeD.Render.IPipeline**
- Den förbakade sekvensen av verksamheter för att dra i GPU sidan, när grafikrörledningen skapas, den underliggande GPU-drivrutinen behöver inte förlänga renderingstillstånd/recompile shaders i ett dragsamtal, som avsevärt kan förbättra renderingsprestandan.
### **Avlägsnade klasser**
- Ta bort klass**Aspose.ThreeD.Render.Renderbar ressource.**
- Basklassen av den minsta renderar uppgiften i gamla rendering arkitektur. Den nya renderaren separerar objektmodellen som är utformad för filläsning/skrivning och implementering av rendering, Så RenderableResource behövs inte längre.


