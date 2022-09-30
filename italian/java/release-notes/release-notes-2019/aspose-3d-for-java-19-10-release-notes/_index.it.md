---
title: Aspose.3D for Java 19.10 Note di rilascio
type: docs
weight: 30
url: /it/java/aspose-3d-for-java-19-10-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 19.10](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.10).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-567 |` ` Problema di conversione RVM e ATT piastrelle|` ` Potenziamento|
|THREEDNET-570 |` ` Il calcolo della scatola di delimitazione delle forme primitive non è corretto|` ` Potenziamento|
|THREEDNET-571 |` ` Esporta forme primitive in file RVM.|` ` Potenziamento|
|THREEDNET-572 |` ` Migliorare il supporto alle esportazioni primitive nello FBX.|` ` Potenziamento|
|THREEDNET-573 |` ` I char speciali nel nome dell'oggetto non possono essere esportati correttamente nel formato FBX|` `Bug|
|THREEDNET-568 |` ` Salvato. I file glb non possono essere aperti.|` `Bug|
|THREEDNET-549|Il caricamento enorme RVM richiede molto tempo e risorse|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Nuovo Class - com.aspose.threed.Dish**
Questa è una nuova forma primitiva parametrizzata.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Dish(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Nuova piramide Class - com.aspose.threed.**
Questa è una nuova forma primitiva parametrizzata.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Nuove proprietà aggiunte alla classe com.aspose.threed.Box**


Le seguenti proprietà sono state aggiunte alla classe Aspose.ThreeD.Entities.Box.

{{< highlight "java" >}}

 /**

\* Gets the length segments.

*/

public int getLengthSegments();

/**

\* Sets the length segments.

\* @param value New value

*/

public void setLengthSegments(int value);

/**

\* Gets the width segments

*/

public int getWidthSegments();

/**

\* Sets the width segments

\* @param value New value

*/

public void setWidthSegments(int value);

/**

\* gets or sets the height segments.

*/

public int getHeightSegments();

/**

\* gets or sets the height segments.

\* @param value New value

*/

public void setHeightSegments(int value);

{{< /highlight >}}
### **Metodo rimosso FindNode in classe com.aspose.threed.Node**
Questo doveva essere rimosso poiché è stato sostituito da SelectSingleObject/SelectObject/SelectObjects più avanzati.
### **Nuovo metodo aggiunto alla classe com.aspose.threed.Node**
Il seguente metodo è stato aggiunto alla classe di nodo Aspose.ThreeD. Che rende più conveniente creare un nodo con un Materiale.

{{< highlight "java" >}}

 /**

\* Create a new child node with given node name, and attach specified entity and a material

\* @param nodeName The new child node's name

\* @param entity Default entity attached to the node

\* @param material The material attached to the node

\* @return The new child node.

*/

public Node createChildNode(String nodeName, Entity entity, Material material);

{{< /highlight >}}

Codice campione

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Box(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Metodi rimossi dalla classe com.aspose.threed.PlyFormat**


I seguenti metodi sono stati sostituiti da PlyFormat.Encode che può essere utilizzato anche per codificare il cloud di punti.



{{< highlight "java" >}}

 private void encodeMesh(IMeshConvertible mesh, Stream stream, PlySaveOptions opt) throws IOException;

private void encodeMesh(IMeshConvertible mesh, String fileName, PlySaveOptions opt) throws IOException;

{{< /highlight >}}
### **Aggiunta nuova proprietà a class com.aspose.threed.FBXSaveOptions**
Questa proprietà rende utile esportare grandi scene composte da primitive.



{{< highlight "java" >}}

 /**

 * Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

*/

public boolean getReusePrimitiveMesh();



/**

\* Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

\* @param value New value

*/

public void setReusePrimitiveMesh(boolean value);

{{< /highlight >}}
#### **Codice campione**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish A", new Dish(), new PbrMaterial(Color.blue));

scene.getRootNode().createChildNode("dish B", new Dish(), new PbrMaterial(Color.blue));

FBXSaveOptions opt = new FBXSaveOptions(FileFormat.FBX7400ASCII);

opt.setReusePrimitiveMesh(true);

scene.save("file.fbx", opt);

{{< /highlight >}}



Poiché le due forme parametrizzate hanno gli stessi parametri, genereranno sicuramente la stessa mesh. Quando questa proprietà è vera, il file FBX generato genererà solo una mesh e la riutilizzerà in nodi diversi.
