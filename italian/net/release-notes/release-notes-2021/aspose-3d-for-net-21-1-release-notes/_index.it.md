---
title: Aspose.3D for .NET 21.1 Note di rilascio
type: docs
weight: 12
url: /it/net/aspose-3d-for-net-21-1-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.1.

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

### Classe aggiunta Aspose.ThreeD.Render.IRenderQueue

Un'istanza IRenderQueue verrà passata a EntityRenderer quando il renderer sta cercando di rendere qualcosa, l'EntityRenderer dovrà prepararsi per le risorse hardware utilizzate per il rendering e aggiungere le attività di rendering alla coda di rendering in EntityRenderer.PrepareRenderQueue


### Classe rimossa Aspose.ThreeD.Render. Irenderabile

Questa è un'interfaccia obsoleta ed è stata utile per molto tempo, è sicuro rimuovere questo.


### Aggiunti nuovi membri alla classe Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}

        /// <summary>
        /// Gets the extension names of this type.
        /// </summary>
        public string[]Extensions{ get;}

        /// <summary>
        /// Universal Scene Description
        /// </summary>
        public static readonly Aspose.ThreeD.FileFormat USD;
{{< /highlight >}}

Alcuni formati come USD, GLTF può contenere più di una estensione, abbiamo introdotto una nuova proprietà per ottenere tutte le estensioni.


### Classe refattorizzata Aspose.ThreeD.Render.EntityRenderer:

{{< highlight "csharp" >}}
        public void PrepareRenderQueue(Aspose.ThreeD.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

È stato cambiato in due funzioni:

{{< highlight "csharp" >}}
        /// <summary>
        /// Prepare rendering commands for specified node/entity pair.
        /// </summary>
        /// <param name="renderer">The current renderer instance</param>
        /// <param name="queue">The render queue used to manage render tasks</param>
        /// <param name="node">Current node</param>
        /// <param name="entity">The entity that need to be rendered</param>
        public void PrepareRenderQueue(Aspose.ThreeD.Render.Renderer renderer, Aspose.ThreeD.Render.IRenderQueue queue, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
        /// <summary>
        /// Each render task pushed to the <see cref="IRenderQueue"/> will have a corresponding RenderEntity call
        /// to perform the concrete rendering job.
        /// </summary>
        /// <param name="renderer">The renderer</param>
        /// <param name="commandList">The commandList used to record the rendering commands</param>
        /// <param name="node">The same node that passed to PrepareRenderQueue of the entity that will be rendered </param>
        /// <param name="renderableResource">The custom object that passed to IRenderQueue during the PrepareRenderQueue </param>
        /// <param name="subEntity">The index of the sub entity that passed to IRenderQueue</param>
        public virtual void RenderEntity(Renderer renderer, ICommandList commandList, Node node, object renderableResource, int subEntity);
{{< /highlight >}}

Nella vecchia implementazione, le risorse hardware utilizzate dal rendering creato durante la fase PrepareRenderQueue, possono causare alcuni problemi in alcuni driver.

Quindi separiamo la preparazione e il rendering e ottimizziamo alcune cache interne.


### Membro obsoleto rimosso dalla classe Aspose.ThreeD.Render.RenderFactory:


{{< highlight "csharp" >}}

        public Aspose.ThreeD.Render.IRenderWindow CreateRenderWindow(Aspose.ThreeD.Render.RenderParameters parameters, System.IntPtr handle)

{{< /highlight >}}

Questa rimozione è stata programmata e questa funzione obsoleta ha una sostituzione con lo stesso nome.

