---
title: Aspose.3D for Java 19.12 Note di rilascio
type: docs
weight: 10
url: /it/java/aspose-3d-for-java-19-12-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 19.12.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|` `**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-590 |` ` Parte della scena persa durante la conversione di un file rvm in file glb|` `Bug|
|THREEDNET-597 |` ` File di caricamento del problema|` `Bug|
|THREEDNET-595 |` `Shadow creato quando la scena viene unita|` `Bug|
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

- Classe rinominata**Com. aspose. tred. curva**A**Com. aspose.threed.KeyframeSequence**
- Classe rinominata**Com. aspose.threed.CurveMapping**A**Com. aspose.threedn.BindPoint**

Tutti i metodi/proprietà correlati sono contrassegnati come obsoleti e verranno rimossi in futuro e vengono forniti nuovi metodi/proprietà.
### **Membri obsoleti in classe com.aspose.threed.AnimationChannel**
{{< highlight "java" >}}

 public void AddCurve(com.aspose.threed.Curve curve)

public IList<com.aspose.threed.Curve> getCurves()

{{< /highlight >}}
#### **Sostituzioni**
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
### **Membri obsoleti in classe com.aspose.threed.AnimationNode**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping findCurveMapping(String name)

public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, String channelName, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.A3DObject target, String propName, boolean create)

public com.aspose.threed.CurveMapping createCurveMapping(com.aspose.threed.A3DObject obj, String propName)

public IList<com.aspose.threed.CurveMapping> getCurveMappings()

{{< /highlight >}}
#### **Sostituzioni**
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
### **Membri obsoleti in classe com.aspose.threed. Proprietà**
{{< highlight "java" >}}

 public com.aspose.threed.CurveMapping getCurveMapping(com.aspose.threed.AnimationNode anim, boolean create)

public com.aspose.threed.Curve getCurve(com.aspose.threed.AnimationNode anim, boolean create)

{{< /highlight >}}
#### **Sostituzioni**
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
### **Membri aggiunti**
Membri aggiunti alla classe**Com. aspose.threed.VertexElementUserData**

{{< highlight "java" >}}

 /**

\* The user data attached in this element

*/

public Map<String, Object> getData();

{{< /highlight >}}

Membri aggiunti alla classe**Com. aspose.threed.RenderFactory**



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

Membri aggiunti alla classe**Com. aspose.threed.Renderer**



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
### **Membri rimossi**
Membri rimossi dalla classe**Com. aspose.threed.RenderFactory**

` ` Il renderer in 19.12 dedurrà automaticamente il layout di memoria del vertice dal vertex shader, non è necessario fornire manualmente i dettagli del layout di memoria del testo. In 19.12 c' è una nuova creazione ShaderProgram fornita che necessita solo di un argomento. Il createRenderState è stato rimosso, ma è stato aggiunto il costruttore di RenderState, è possibile creare RenderState utilizzando il suo costruttore predefinito.



{{< highlight "java" >}}

 public ShaderProgram createShaderProgram(ShaderSource shaderSource, List<VertexField> inputFields);

public ShaderProgram createShaderProgram(ShaderSource shaderSource, VertexDeclaration vertexDeclaration);

public RenderState createRenderState();

{{< /highlight >}}

Membri rimossi dalla classe**Com. aspose.threed.Render.Renderer**

Questi membri rimossi sono correlati al rendering di basso livello, in 19.12 EntityRenderer e ICommandList saranno responsabili delle implementazioni di rendering.

{{< highlight "java" >}}

 public void bindRenderState(com.aspose.threed.RenderState renderState)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer, int count)

public void Draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, int first, int count)

public void draw(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer)

public void drawIndexed(com.aspose.threed.DrawOperation drawOperation, com.aspose.threed.IVertexBuffer vertexBuffer, com.aspose.threed.IIndexBuffer indexBuffer)

public void submitRenderTask(com.aspose.threed.RenderQueueGroupId groupId, int priority, com.aspose.threed.Node node, com.aspose.threed.IRenderable renderableTask)

{{< /highlight >}}



- Rimosso enum**Com. aspose.threed.VariableSemantic**
-Il renderer in 19.12 non gestirà più la variabile shader, invece, ogni implementazione del renderer di entità fornirà manualmente i dati necessari allo shader tramite push costante o buffer uniforme, questo rende il renderer più efficiente e più semplice.
- Membro rimosso da**Com. aspose.threed.ShaderVariable**
-Variabile pubblica Semantica {get;}
- Membri rimossi dalla classe**Com. aspose.threed.ShaderProgram**
-IList pubblico<Aspose.ThreeD.Render.ShaderVariable>Variabili {get;set;}
### **Classi aggiunte**
- Classe aggiunta**Com. aspose.threed.EntityRenderer**
-Sottoclasse questo per fornire l'implementazione del rendering per le entità specificate.
- Classe aggiunta**Com. aspose.threed.ICommandList**
-L'EntityRenderer sottocllased utilizza ICommandList per codificare le istruzioni per rendere l'entità.
- Classe aggiunta**Com. aspose.threed.IDescriptorSet**
-Il set di descrittori è un insieme di descrittori, un descrittore può essere un buffer uniforme, un'unità texture o altre risorse laterali GPU. Se più entità condividono la stessa pipeline grafica ma con trame e altri dati diversi, possono utilizzare IDescriptorSet per fornire dati per entità.
- Classe aggiunta**Com. aspose.threed.DescriptorSetUpdater**
-L'IDescriptorSet non fornisce un'interfaccia per modificare i suoi descrittori limitati, è necessario un DescriptorSetUpdater per impegnare più aggiornamenti alla GPU.
- Classe aggiunta**Com. aspose.threed. RenderVariableManager**
-Quando si esegue il rendering manuale di un'entità, di solito sono necessarie alcune variabili interne come la matrice di visualizzazione/proiezione, queste possono essere trovate su RendererVariableManager.
- Classe aggiunta**Com. aspose.threed.SPIRV Source**
-Quando si crea un'istanza del programma shader, è necessaria l'origine SPIR-V, SPIR-V è il codice byte per Vulkan compilato da GLSL o altri linguaggi shader.
- Classe aggiunta**Com. aspose.threed.IOUtils**
-Ha fornito alcuni metodi di estensione per scrivere matrice/vettore a BinaryWriter.
- Classe aggiunta**Com. aspose.threed.IPipeline**
-La sequenza di operazioni precaked da disegnare sul lato GPU, quando viene creata la pipeline grafica, il driver GPU sottostante non avrà bisogno di riconvalidare lo stato di rendering/ricompilare gli shader in una chiamata di estrazione, il che può migliorare notevolmente le prestazioni di rendering.
### **Classi rimosse**
- Classe rimossa**Aspose.ThreeD.Render.RenderableResource**
-La classe base del minimo rende l'attività nella vecchia architettura di rendering. Il nuovo renderer separa il modello a oggetti progettato per la lettura/scrittura dei file e l'implementazione del rendering, quindi RenderableResource non è più necessario.
