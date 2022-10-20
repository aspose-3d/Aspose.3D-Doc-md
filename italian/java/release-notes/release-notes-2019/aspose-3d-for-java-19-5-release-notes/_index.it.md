---
title: Aspose.3D for Java 19.5 Note di rilascio
type: docs
weight: 80
url: /it/java/aspose-3d-for-java-19-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 19.5](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.5)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-501|Integrare con l'ultimo Dynabic.Metered|Miglioramento|
|THREEDNET-505|Consenti l'orientamento del cambio aereo specificando una normale|Miglioramento|
|THREEDNET-489|Shadow non funziona nel renderer Vulkan|Bug|
|THREEDNET-504|Draco creato dal file STL è rotto|Bug|

## **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

**Aggiunta nuova proprietà * Raggio * in classe com.aspose.threed.Plane**

{{< highlight "java" >}}

 /**

 * Gets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 */

public Vector3 getUp();

/**

 * Sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 * @param value New value

 */

public void setUp(Vector3 value);

{{< /highlight >}}

Codice di esempio per specificare il raggio per proprietà piuttosto che l'argomento del costruttore:

{{< highlight "java" >}}

 Scene scene = new Scene();

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

scene.getRootNode().createChildNode(plane);

//This will generate a plane that has customized orientation

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Aggiunto il nuovo metodo "getConsumptionCredit" nella classe com.aspose.threed.Metered**

{{< highlight "java" >}}

 /**

\* Gets consumption credit

\* @return consumption quantity

*/

public static double getConsumptionCredit() throws Exception;

{{< /highlight >}}

Ottiene il credito di consumo del mese corrente, utilizzato dal servizio di fatturazione Dynabic.Metered.
