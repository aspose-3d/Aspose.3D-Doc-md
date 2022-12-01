---
title: Aspose.3D for .NET 19.12 Note di rilascio
type: docs
weight: 10
url: /it/net/aspose-3d-for-net-19-12-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 19.12.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|` `**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-590 |` ` Parte della scena persa durante la conversione di un file rvm in file glb|` `Bug|
|THREEDNET-597 |` ` File di caricamento del problema|` `Bug|
|THREEDNET-595 |` `Shadow creato quando una scena viene unita|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
Questa versione ha due principali modifiche API:

- Rifattorizzato il sistema di animazione, quindi possiamo prenotare alcuni nomi per l'uso futuro quando saranno supportati i formati CAD.
-Questa versione rinominata**Curva**A**KeyframeSequence**, E**CurveMapping**A**Punto di bindpoint**. Le interfacce obsolete saranno rimosse dallo Aspose.3D for .NET 20.03. I metodi che utilizzano queste classi forniranno la sostituzione come alternativa.
-Mentre i vecchi nomi sono ancora esistenti in 19.12, il codice che si basa su queste modifiche ha bisogno di meno o addirittura nessuna modifica (se si utilizza tipo inferire).
- Rimosso il renderer legacy OpenGL e rifattorizzato il renderer in modo che funzioni meglio con il driver Vulkan sottostante. Le interfacce di basso livello sono state modificate mantenendo intatte le interfacce di rendering di alto livello.
-Il renderer refactored ha migliori prestazioni di rendering, con maggiore flessibilità ed estensibilità.
-Il metodo di rendering nel**Scena**La classe non ha cambiamenti. Se si utilizza un'interfaccia di rendering di alto livello, non è necessario modificare nulla.
-Il basso livello API ha un cambiamento di rottura, potrebbe essere necessario contattare il supporto per la migrazione del codice.

Di seguito sono riportate le informazioni dettagliate sulle modifiche al pubblico API in questa versione.

- Classe rinominata**Aspose.ThreeD. Animazione. Curve**A**Aspose.ThreeD. Animazione. KeyframeSequence**
- Classe rinominata**Aspose.ThreeD. Animazione. CurveMapping**A**Aspose.ThreeD. Animazione. BindPoint**

Tutti i metodi/proprietà correlati sono contrassegnati come obsoleti e verranno rimossi in futuro e vengono forniti nuovi metodi/proprietà.
### **Membri obsoleti in classe Aspose.ThreeD.Animation.AnimationChannel**
- Void pubblico AddCurve(Aspose.ThreeD. Animazione. Curva)
- IList pubblica<Aspose.ThreeD.Animation.Curve>Curve {get;}
#### **Sostituzioni**
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


### **Membri obsoleti in classe Aspose.ThreeD. Animazione. Nodo di animazione**
{{< highlight "java" >}}

 public Aspose.ThreeD.Animation.CurveMapping FindCurveMapping(string name)

public Aspose.ThreeD.Animation.CurveMapping GetCurveMapping(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, string channelName, bool create)

public Aspose.ThreeD.Animation.Curve GetCurve(Aspose.ThreeD.A3DObject target, string propName, bool create)

public Aspose.ThreeD.Animation.CurveMapping CreateCurveMapping(Aspose.ThreeD.A3DObject obj, string propName)

public IList<Aspose.ThreeD.Animation.CurveMapping> CurveMappings{ get;}

{{< /highlight >}}
#### **Sostituzioni**
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
### **Membri obsoleti in classe Aspose.ThreeD. Proprietà**
- Pubblico Aspose.ThreeD. Animazione. CurveMapping GetCurveMapping(Aspose.ThreeD. Animazione. AnimationNode anim, bool creare)
- Pubblico Aspose.ThreeD. Animazione. Curve GetCurve(Aspose.ThreeD. Animazione. AnimationNode anim, bool crean)
#### **Sostituzioni**
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
### **Membri aggiunti**
` ` Membri aggiunti alla classe**Aspose.ThreeD. Entità. VertexElementUserData**

{{< highlight "java" >}}

 /// <summary>

/// The user data attached in this element

/// </summary>

public Dictionary<string, object> Data{ get;}

{{< /highlight >}}

Membri aggiunti alla classe**Aspose.ThreeD.Render.RenderFactory**

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

Membri aggiunti alla classe**Aspose.ThreeD. Renderer. Renderer**

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


### **Membri rimossi**
Classe rimossa**Aspose.ThreeD.Render.RenderableResource**

La classe base dell'attività di rendering minimo nella vecchia architettura di rendering. Il nuovo renderer separa il modello a oggetti progettato per la lettura/scrittura dei file e l'implementazione del rendering, quindi RenderableResource non è più necessario.

{{< highlight "java" >}}

 public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, IList<VertexField> inputFields);

public ShaderProgram CreateShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState CreateRenderState();

{{< /highlight >}}

Membri rimossi dalla classe**Aspose.ThreeD. Renderer. Renderer**

Questi membri rimossi sono correlati al rendering di basso livello, in 19.12 EntityRenderer e ICommandList saranno responsabili delle implementazioni di rendering.

{{< highlight "java" >}}

 public void BindRenderState(Aspose.ThreeD.Render.RenderState renderState)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, int first, int count)

public void Draw(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer)

public void DrawIndexed(Aspose.ThreeD.Render.DrawOperation drawOperation, Aspose.ThreeD.Render.IVertexBuffer vertexBuffer, Aspose.ThreeD.Render.IIndexBuffer indexBuffer)

public void SubmitRenderTask(Aspose.ThreeD.Render.RenderQueueGroupId groupId, int priority, Aspose.ThreeD.Node node, Aspose.ThreeD.Render.IRenderable renderableTask)

public Aspose.ThreeD.Render.Renderer CurrentContext{ get;}

{{< /highlight >}}

- Rimosso enum**Aspose.ThreeD.Render.VariableSemantic**
-Il renderer in 19.12 non gestirà più la variabile shader, invece, ogni implementazione del renderer di entità fornirà manualmente i dati necessari allo shader tramite push costante o buffer uniforme, questo rende il renderer più efficiente e più semplice.
- Membro rimosso da**Aspose.ThreeD.Render. ShaderVariabile**
-Variabile pubblica Semantica {get;}
- Membri rimossi dalla classe**Aspose.ThreeD.Render.ShaderProgram**
-IList pubblico<Aspose.ThreeD.Render.ShaderVariable>Variabili {get;set;}
- Classe rimossa**Aspose.ThreeD.Render.RenderableResource**
-La classe base del minimo rende l'attività nella vecchia architettura di rendering. Il nuovo renderer separa il modello a oggetti progettato per la lettura/scrittura dei file e l'implementazione del rendering, quindi RenderableResource non è più necessario.
### **Classi aggiunte**
- Classe aggiunta**Aspose.ThreeD.Render.EntityRenderer**
-Sottoclasse questo per fornire l'implementazione del rendering per le entità specificate.
- Classe aggiunta**Aspose.ThreeD.Render.ICommandList**
-L'EntityRenderer sottocllased utilizza ICommandList per codificare le istruzioni per rendere l'entità.
- Classe aggiunta**Aspose.ThreeD.Render.IDescriptorSet**
-Il set di descrittori è un insieme di descrittori, un descrittore può essere un buffer uniforme, un'unità texture o altre risorse laterali GPU. Se più entità condividono la stessa pipeline grafica ma con trame e altri dati diversi, possono utilizzare IDescriptorSet per fornire dati per entità.
- Classe aggiunta**Aspose.ThreeD.Render.DescriptorSetUpdater**
-L'IDescriptorSet non fornisce un'interfaccia per modificare i suoi descrittori limitati, è necessario un DescriptorSetUpdater per impegnare più aggiornamenti alla GPU.
- Classe aggiunta**Aspose.ThreeD.Render. RenderVariableManager**
-Quando si esegue il rendering manuale di un'entità, di solito sono necessarie alcune variabili interne come la matrice di visualizzazione/proiezione, queste possono essere trovate su RendererVariableManager.
- Classe aggiunta**Aspose.ThreeD.Render.SPIRV Source**
-Quando si crea un'istanza del programma shader, è necessaria l'origine SPIR-V, SPIR-V è il codice byte per Vulkan compilato da GLSL o altri linguaggi shader.
- Classe aggiunta**Aspose.ThreeD. Utenze. IOUtils**
-Ha fornito alcuni metodi di estensione per scrivere matrice/vettore a BinaryWriter.
- Classe aggiunta**Aspose.ThreeD.Render. IPpipeline**
-La sequenza di operazioni precaked da disegnare sul lato GPU, quando viene creata la pipeline grafica, il driver GPU sottostante non avrà bisogno di riconvalidare lo stato di rendering/ricompilare gli shader in una chiamata di estrazione, il che può migliorare notevolmente le prestazioni di rendering.
### **Classi rimosse**
- Classe rimossa**Aspose.ThreeD.Render.RenderableResource**
-La classe base del minimo rende l'attività nella vecchia architettura di rendering. Il nuovo renderer separa il modello a oggetti progettato per la lettura/scrittura dei file e l'implementazione del rendering, quindi RenderableResource non è più necessario.


