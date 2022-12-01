---
title: Aspose.3D for .NET 19.10 Note di rilascio
type: docs
weight: 30
url: /it/net/aspose-3d-for-net-19-10-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per Aspose.3D for .NET 19.10.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-567 |` ` Problema di conversione RVM e ATT piastrelle|Miglioramento|
|THREEDNET-570 |` ` Il calcolo della scatola di delimitazione delle forme primitive non è corretto|Miglioramento|
|THREEDNET-571 |` ` Esporta forme primitive in file RVM.|Miglioramento|
|THREEDNET-572 |` ` Migliorare il supporto alle esportazioni primitive nello FBX.|Miglioramento|
|THREEDNET-573 |` ` I char speciali nel nome dell'oggetto non possono essere esportati correttamente nel formato FBX|Bug|
|THREEDNET-568 |` ` Salvato. I file glb non possono essere aperti.|Bug|
|THREEDNET-549|Il caricamento enorme RVM richiede molto tempo e risorse|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Nuova classe-Aspose.ThreeD. Entità. Piatto**
Questa è una nuova forma primitiva parametrizzata.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish", new Dish(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **Nuova classe-Aspose.ThreeD. Entità. Piramide**
Questa è una nuova forma primitiva parametrizzata.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **Nuove proprietà aggiunte alla classe Aspose.ThreeD.Entities.Box**


Le seguenti proprietà sono state aggiunte alla classe Aspose.ThreeD.Entities.Box.

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the length segments.

/// </summary>

public int LengthSegments{ get;set;}

/// <summary>

/// Gets or sets the width segments

/// </summary>

public int WidthSegments{ get;set;}

/// <summary>

/// gets or sets the height segments.

/// </summary>

public int HeightSegments{ get;set;}

{{< /highlight >}}
### **Metodo rimosso FindNode in classe Aspose.ThreeD. Nodo**
Questo doveva essere rimosso poiché è stato sostituito da SelectSingleObject/SelectObject/SelectObjects più avanzati.
### **Nuovo metodo aggiunto alla classe Aspose.ThreeD. Nodo**
Il seguente metodo è stato aggiunto alla classe di nodo Aspose.ThreeD. Che rende più conveniente creare un nodo con un Materiale.

{{< highlight "java" >}}

 /// <summary>

/// Create a new child node with given node name, and attach specified entity and a material

/// </summary>

/// <param name="nodeName">The new child node's name</param>

/// <param name="entity">Default entity attached to the node</param>

/// <param name="material">The material attached to the node</param>

/// <returns>The new child node.</returns>

public Node CreateChildNode(string nodeName, Entity entity, Material material);

{{< /highlight >}}

Codice campione

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("box", new Box(), new PbrMaterial(Color.Coral));

{{< /highlight >}}

Metodi rimossi dalla classe Aspose.ThreeD. Formati. PlyFormat

I seguenti metodi sono stati sostituiti da PlyFormat.Encode che può essere utilizzato anche per codificare il cloud di punti.



{{< highlight "java" >}}

 public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, System.IO.Stream stream, Aspose.ThreeD.Formats.PlySaveOptions opt);

public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, string fileName, Aspose.ThreeD.Formats.PlySaveOptions opt);

{{< /highlight >}}

Aggiunta nuova proprietà alla classe Aspose.ThreeD.Formats.FBXSaveOptions

Questa proprietà rende utile esportare grandi scene composte da primitive.



{{< highlight "java" >}}

 /// <summary>

/// Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

/// Default value is false

/// </summary>

public bool ReusePrimitiveMesh { get; set; }

{{< /highlight >}}
#### **Codice campione**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish A", new Dish(), new PbrMaterial(Color.Coral));

scene.RootNode.CreateChildNode("dish B", new Dish(), new PbrMaterial(Color.Coral));

scene.Save("file.fbx", new FBXSaveOptions(FileFormat.FBX7400ASCII) { ReusePrimitiveMesh = true });

{{< /highlight >}}



Poiché le due forme parametrizzate hanno gli stessi parametri, genereranno sicuramente la stessa mesh. Quando questa proprietà è vera, il file FBX generato genererà solo una mesh e la riutilizzerà in nodi diversi.
