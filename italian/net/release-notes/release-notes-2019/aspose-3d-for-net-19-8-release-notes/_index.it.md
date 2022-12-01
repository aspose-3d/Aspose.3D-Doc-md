---
title: Aspose.3D for .NET 19.8 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-3d-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.8](/3d/it/net/aspose-3d-for-net-19-8-release-notes/)

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
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Aggiunta nuova proprietà PointCloud nella classe Aspose.ThreeD.Formats.ObjSaveOptions**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

/// </summary>

public bool PointCloud

{

    get;set;

}

{{< /highlight >}}

Codice di esempio per generare una nuvola di punti di Sfera in formato obj.

{{< highlight "java" >}}

 var scene = new Scene(new Sphere());

scene.Save(@"sphere.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
### **Aggiunti nuovi metodi CreatePolygon Aspose.ThreeD.Entities.Mesh**
{{< highlight "java" >}}

 /// <summary>

/// Create a polygon with 4 vertices(quad)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

/// <param name="v4">Index of the fourth vertex</param>

public void CreatePolygon(int v1, int v2, int v3, int v4);

/// <summary>

/// Create a polygon with 3 vertices(triangle)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

public void CreatePolygon(int v1, int v2, int v3);

{{< /highlight >}}

Codice del campione.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.CreatePolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

I nuovi metodi aggiunti**CreatePolygon**Ti permettono di creare un triangolo o un quad senza allocare memoria extra, è altamente ottimizzato internamente.


### **Rimosso il vecchio campo pubblico PrettyPrint nella classe Aspose.ThreeD. Formati. GLTFSaveOptions**
Questo è stato rimosso e sostituito dalla proprietà con lo stesso nome, quindi il codice legacy che lo utilizzava non ha bisogno di modifiche.
### **Aggiunta nuova proprietà PrettyPrint nella classe Aspose.ThreeD.Formats.GLTFSaveOptions**

{{< highlight "java" >}}

 /// <summary>

/// The JSON content of GLTF file is indented for human reading, default value is false

/// </summary>

public bool PrettyPrint { get; set; }

{{< /highlight >}}

Il vecchio**PrettyPrint**Era un campo pubblico ed è stato sostituito dalla proprietà per coerente.
