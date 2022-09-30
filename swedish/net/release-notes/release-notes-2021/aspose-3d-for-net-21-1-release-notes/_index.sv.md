---
title: Aspose.3D for .NET 21,1 Utgivning
type: docs
weight: 12
url: /sv/net/aspose-3d-for-net-21-1-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.1.

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

### Tillagd klass Aspose.ThreeD.Render.IRenderQueue

En IRenderQueue instans kommer att skickas till EntityRenderer när renderande försöker göra något, EntityRenderer kommer att behöva förbereda sig för de hårdvarresurser som används för att rendera och lägga till renderingsuppgifterna i renderingskön i EntityRenderer. FörberedRenderQueue


### Avlägsnad klass Aspose.ThreeD.

Detta är ett föråldrat gränssnitt och var användbart under en lång tid, det är säkert att ta bort detta.


### Lagt till nya medlemmar i klass Aspose.ThreeD.FileFormat:

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

Vissa format som USD, GLTF kan innehålla mer än en tillägg, Vi introducerade en ny egendom för att få alla tillägg.


### Refactorerad klass Aspose.ThreeD.Render.EntityRender:

{{< highlight "csharp" >}}
        public void PrepareRenderQueue(Aspose.ThreeD.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

Har ändrats till två funktioner:

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

I det gamla genomförandet, de hårdvarresurser som används av rendering skapades under steget PrepareRenderQueue, kan orsaka vissa problem hos vissa förare.

Så vi separerade förberedelsen och återgivningen, och optimerade några inre cacher.


### Föråldrad medlem avlägsnad från klass Aspose.ThreeD.RenderFactory:


{{< highlight "csharp" >}}

        public Aspose.ThreeD.Render.IRenderWindow CreateRenderWindow(Aspose.ThreeD.Render.RenderParameters parameters, System.IntPtr handle)

{{< /highlight >}}

Denna borttagning var schemalagd, och denna föråldrade funktion har en ersättning med samma namn.

