---
title: Aspose.3D for Java 19.4 Note di rilascio
type: docs
weight: 90
url: /it/java/aspose-3d-for-java-19-4-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 19.4](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.4)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-483 |Supporto per il formato VRML|Nuova funzionalità|
|THREEDJAVA-26|Supporto per rendering per Aspose.3D for Java|Nuova funzionalità|
|THREEDNET-496 |Problema di corruzione delle esportazioni FBX7500Binarie|Bug|

## **Pubblico API e modifiche incompatibili arretrate**

Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

**Aggiunta nuova proprietà Radius in classe com.aspose.threed.Sphere**

{{< highlight "java" >}}

 /**

 * Gets the radius of the sphere.

 */

public double getRadius();

/**

 * Sets the radius of the sphere.

 * @param value New value

 */

public void setRadius(double value);

{{< /highlight >}}

Codice di esempio per specificare il raggio per proprietà piuttosto che l'argomento del costruttore:

{{< highlight "java" >}}

 Scene scene = new Scene();

Sphere sphere = new Sphere();

sphere.setRadius(10);

scene.getRootNode().createChildNode(sphere);

scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Aggiunto nuovo formato di file VRML in classe com.aspose.threed.FileFormat e com.aspose.threed.FileFormatType**

{{< highlight "java" >}}

 /**

 * The Virtual Reality Modeling Language

 */

public static final FileFormat VRML;

{{< /highlight >}}

Aspose.3D può rilevare automaticamente il formato VRML, quindi il FileFormat viene solitamente ignorato nel metodo Open. Codice del campione:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.open("test.wrl");

{{< /highlight >}}
