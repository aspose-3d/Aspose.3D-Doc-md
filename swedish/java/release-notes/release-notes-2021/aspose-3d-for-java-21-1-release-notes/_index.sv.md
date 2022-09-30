---
title: Aspose.3D for Java 21,1 Utgivning
type: docs
weight: 12
url: /sv/java/aspose-3d-for-java-21-1-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.1.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-784 |Lägg till stöd för USDC-format|Ny funktion|
|THREEDNET-773 |Lägg till materialstöd för filen DXF|Förbättring|
|THREEDNET-797 |Lägg till stöd för . Netto 5.0|Förbättring|
|THREEDNET-803 |Förbättra kombinationsrutan i webben renderare.|Förbättring|
|THREEDNET-795 |Obj till u3d konvertering - saknad textur.|Felrättning|
|THREEDNET-801 |Implementeringen av kamerans ortografiska projektion är felaktig|Felrättning|
|THREEDNET-783 |Karta bitmap till trianglar från GLB.|Felrättning|
|THREEDNET-802 |Draco/glTF Filer som används förutsägelsegradsalgoritm kommer inte att importera.|Felrättning|
|THREEDNET-804 |Aspose.3D rendering fungerar inte på någon integrerad GPU.|Felrättning|



## API ändringar ##

Två stora förändringar i 21,1.

* Renderer's prestanda förbättras genom att separera beredning och rendering, även fixade några rendering relaterade fel.
* Tillagd stöd för import av USDC

### Tillagd klass `com.aspose.threed.IRenderQueue`

En IRenderQueue instans kommer att skickas till EntityRenderer när renderande försöker göra något, EntityRenderer kommer att behöva förbereda sig för de hårdvarresurser som används för att rendera och lägga till renderingsuppgifterna i renderingskön i EntityRenderer. FörberedRenderQueue


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



### Avlägsnad klass `com.aspose.threed.IRenderable`

Detta är ett föråldrat gränssnitt och var användbart under en lång tid, det är säkert att ta bort detta.


### Lagt till nya medlemmar i klass `com.aspose.threed.FileFormat`:

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

Vissa format som USD, GLTF kan innehålla mer än en tillägg, Vi introducerade en ny egendom för att få alla tillägg.


### Refaktorerad klass `com.aspose.threed.EntityRenderer`:

{{< highlight "java" >}}
        public void prepareRenderQueue(com.aspose.threed.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

Har ändrats till två funktioner:

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

I det gamla genomförandet, de hårdvarresurser som används av rendering skapades under steget PrepareRenderQueue, kan orsaka vissa problem hos vissa förare.

Så vi separerade förberedelsen och återgivningen, och optimerade några inre cacher.


### Föråldrad medlem bort från klass `com.aspose.threed.RenderFactory`:


{{< highlight "java" >}}

        public com.aspose.threed.IRenderWindow createRenderWindow(com.aspose.threed.RenderParameters parameters, long handle);

{{< /highlight >}}

Denna borttagning var schemalagd, och denna föråldrade funktion har en ersättning med samma namn.

