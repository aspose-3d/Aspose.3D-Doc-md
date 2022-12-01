---
title: Aspose.3D for Java 19.1 Note di rilascio
type: docs
weight: 120
url: /it/java/aspose-3d-for-java-19-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per Aspose.3D for Java 19.1.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Riassunto**|**Categoria**|
|:- |:- |
|Algoritmo di atlante UV|Nuova funzione|
|AMF Esportatore|Nuova funzione|
|Rilevamento del formato file basato su archivio|Nuova funzione|

## **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

**Aggiunta classe com.aspose.threed.AMFSaveOptions:**

{{< highlight "java" >}}

 /**

 * Save options for AMF

 */

public class AMFSaveOptions extends SaveOptions

{ 



    /**

     * Whether to use compression to reduce the final file size, default value is true

     */

    public boolean getEnableCompression();



    /**

     * Whether to use compression to reduce the final file size, default value is true

     * @param value New value

     */

    public void setEnableCompression(boolean value);

}

{{< /highlight >}}

**Nuovo membro aggiunto alla classe «com.aspose.threed.PolygonModifier':**

{{< highlight "java" >}}

     /**

     * Generate UV data from the given input mesh and specified normal data.

     * @param mesh The input mesh

     * @param normals The normal data

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh, VertexElementNormal normals);

    /**

     * Generate UV data from the given input mesh

     * @param mesh The input mesh

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh);

{{< /highlight >}}




