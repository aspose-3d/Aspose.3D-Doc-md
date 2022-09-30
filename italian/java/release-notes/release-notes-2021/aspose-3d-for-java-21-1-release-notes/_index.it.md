---
title: Aspose.3D for Java 21.1 Note di rilascio
type: docs
weight: 12
url: /it/java/aspose-3d-for-java-21-1-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.1.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-784 |Aggiungere il supporto del formato USDC|Nuova funzionalità|
|THREEDNET-773 |Aggiungi supporto materiale per il file DXF|Miglioramento|
|THREEDNET-797 |Aggiungi supporto per. Netto 5.0|Miglioramento|
|THREEDNET-803 |Migliorare ComboBox nel renderer web.|Miglioramento|
|THREEDNET-795 |Conversione da obj a u3d-texture mancante|Correzione di bug|
|THREEDNET-801 |L'implementazione della proiezione ortografica della fotocamera non è corretta|Correzione di bug|
|THREEDNET-783 |Mappa bitmap a triangoli da GLB.|Correzione di bug|
|THREEDNET-802 |Draco/glTF L'algoritmo di previsione dei file utilizzati non è riuscito a importare.|Correzione di bug|
|THREEDNET-804 |Il rendering Aspose.3D non funziona su alcune GPU integrate|Correzione di bug|



## API modifiche ##

Ci sono due grandi cambiamenti nel 21.1,

* Le prestazioni di Renderer sono migliorate separando la preparazione e il rendering, inoltre hanno risolto alcuni bug relativi al rendering.
* Aggiunto il supporto dell'importazione USDC

### Classe aggiunta `com.aspose.threed.IRenderQueue`

Un'istanza IRenderQueue verrà passata a EntityRenderer quando il renderer sta cercando di rendere qualcosa, l'EntityRenderer dovrà prepararsi per le risorse hardware utilizzate per il rendering e aggiungere le attività di rendering alla coda di rendering in EntityRenderer.PrepareRenderQueue


{{< highlight "java" >}}
/**
 * Entity renderer uses this queue to manage render tasks.
 */
public interface IRenderQueue
{    
    /**
     * Add render task to the render queue.
     * @param groupId Which group of the queue the render task will be in
     * @param pipeline The pipeline instance used for this render task
     * @param renderableResource Custom object that will be sent to EntityRenderer.RenderEntity
     * @param subEntity The index of sub entities, useful when the entity is consisting of more than one sub renderable components.
     */
    void add(RenderQueueGroupId groupId, IPipeline pipeline, Object renderableResource, int subEntity);
}
{{< /highlight >}}



### Classe rimossa `com.aspose.threed.IRenderable`

Questa è un'interfaccia obsoleta ed è stata utile per molto tempo, è sicuro rimuovere questo.


### Aggiunti nuovi membri alla classe `com.aspose.threed.FileFormat`:

{{< highlight "java" >}}
    /**
     * Gets the extension name of this type.
     */
    public String[]getExtensions();

    /**
     * Universal Scene Description
     */
    public static final FileFormat USD;

{{< /highlight >}}

Alcuni formati come USD, GLTF può contenere più di una estensione, abbiamo introdotto una nuova proprietà per ottenere tutte le estensioni.


### Classe refattorizzata `com.aspose.threed.EntityRenderer`:

{{< highlight "java" >}}
        public void prepareRenderQueue(com.aspose.threed.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

È stato cambiato in due funzioni:

{{< highlight "java" >}}

    /**
     * Prepare rendering commands for specified node/entity pair.
     * @param renderer The current renderer instance
     * @param queue The render queue used to manage render tasks
     * @param node Current node
     * @param entity The entity that need to be rendered
     */
    public void prepareRenderQueue(Renderer renderer, IRenderQueue queue, Node node, Entity entity);
    
    /**
     * Each render task pushed to the {@link com.aspose.threed.IRenderQueue} will have a corresponding RenderEntity call
     * to perform the concrete rendering job.
     * @param renderer The renderer
     * @param commandList The commandList used to record the rendering commands
     * @param node The same node that passed to PrepareRenderQueue of the entity that will be rendered
     * @param renderableResource The custom object that passed to IRenderQueue during the PrepareRenderQueue
     * @param subEntity The index of the sub entity that passed to IRenderQueue
     */
    public void renderEntity(Renderer renderer, ICommandList commandList, Node node, Object renderableResource, int subEntity);
{{< /highlight >}}

Nella vecchia implementazione, le risorse hardware utilizzate dal rendering creato durante la fase PrepareRenderQueue, possono causare alcuni problemi in alcuni driver.

Quindi separiamo la preparazione e il rendering e ottimizziamo alcune cache interne.


### Membro obsoleto rimosso dalla classe `com.aspose.threed.RenderFactory`:


{{< highlight "java" >}}

        public com.aspose.threed.IRenderWindow createRenderWindow(com.aspose.threed.RenderParameters parameters, long handle);

{{< /highlight >}}

Questa rimozione è stata programmata e questa funzione obsoleta ha una sostituzione con lo stesso nome.

