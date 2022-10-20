---
title: Aspose.3D for Java 19.8 Note di rilascio
type: docs
weight: 50
url: /it/java/aspose-3d-for-java-19-8-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 19.8](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.8)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-528|Aggiungere il supporto della nuvola di punti nel Wavefront OBJ|Nuova funzione|
|THREEDNET-531|Revisione della sicurezza dello Aspose.3D|Miglioramento|
|THREEDNET-536 |Errore di conversione da DRC a STL|Bug|
|THREEDNET-537|Problema di conversione da PLY a GLB|Bug|
|THREEDNET-539|La nuvola di grandi punti può generare dati errati|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Aggiunto nuovo getter/setter PointCloud nella classe com.aspose.threed.ObjSaveOptions**
{{< highlight "java" >}}

 /**

 * Gets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 */

public boolean getPointCloud();

/**

 * Sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 * @param value New value

 */

public void setPointCloud(boolean value);

{{< /highlight >}}

Codice di esempio per generare una nuvola di punti di Sfera in formato obj.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

ObjSaveOptions opt = new ObjSaveOptions();

opt.setPointCloud(true);

scene.save("sphere.obj", opt);

{{< /highlight >}}
### **Aggiunti nuovi metodi createPolygon com.aspose.threed.Mesh**
{{< highlight "java" >}}

 /**

 * Create a polygon with 4 vertices(quad)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 * @param v4 Index of the fourth vertex

 */

public void createPolygon(int v1, int v2, int v3, int v4);

/**

 * Create a polygon with 3 vertices(triangle)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 */

public void createPolygon(int v1, int v2, int v3);

{{< /highlight >}}

Codice del campione.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.createPolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.createPolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

I nuovi metodi aggiunti**CreatePoligono**Ti permettono di creare un triangolo o un quad senza allocare memoria extra, è altamente ottimizzato internamente.


### **Rimosso il vecchio campo pubblico prettyPrint in classe com.aspose.threed.GLTFSaveOptions**
Questo è stato rimosso e sostituito dalla proprietà con lo stesso nome.
### **Aggiunto il nuovo getter/setter PrettyPrint nella classe com.aspose.threed.GLTFSaveOptions**
{{< highlight "java" >}}

 /**

\* The JSON content of GLTF file is indented for human reading, default value is false

*/

public boolean getPrettyPrint();

/**

\* The JSON content of GLTF file is indented for human reading, default value is false

\* @param value New value

*/

public void setPrettyPrint(boolean value);

{{< /highlight >}}

Il vecchio**Stampa carina**Era un campo pubblico ed è stato sostituito dalla proprietà per coerente.

Codice del campione.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//opt.prettyPrint = true; //Old code

opt.setPrettyPrint(true); //Use setter to change this configuration.

scene.save("sphere.gltf", opt);

{{< /highlight >}}




