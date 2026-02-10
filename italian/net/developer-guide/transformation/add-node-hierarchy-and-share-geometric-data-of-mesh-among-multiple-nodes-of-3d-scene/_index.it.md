---
title: Aggiungi la gerarchia dei nodi e condividi i dati geometrici della mesh tra più nodi della scena 3D
type: docs
weight: 40
url: /it/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET offre la creazione di una gerarchia dei Nodi. Il Nodo è l'elemento costitutivo di base di una scena. Una gerarchia di nodi definisce la struttura logica di una scena e fornisce contenuto visibile collegando geometrie, luci e telecamere ai nodi.
---
##  **Aggiungi la gerarchia dei nodi nel documento della scena 3D**
Aspose.3D for .NET offre la creazione di una gerarchia dei Nodi. Il Nodo è l'elemento costitutivo di base di una scena. Una gerarchia di nodi definisce la struttura logica di una scena e fornisce contenuto visibile collegando geometrie, luci e telecamere ai nodi.
###  **Esempio di grafico della scena**
Una gerarchia di scene campione assomiglia a:

! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D, ogni istanza `Node` può avere più nodi figlio, in questo esempio, abbiamo creato un nodo con due nodi cubo, se ruotiamo il nodo radice, anche tutti i nodi figlio vengono interessati:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Get a child node object
Node top = scene.RootNode.CreateChildNode();
// Each cube node has their own translation
Node cube1 = top.CreateChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();            
// Point node to the mesh
cube1.Entity = mesh;
// Set first cube translation
cube1.Transform.Translation = new Vector3(-10, 0, 0);
Node cube2 = top.CreateChildNode("cube2");
// Point node to the mesh
cube2.Entity = mesh;
// Set second cube translation
cube2.Transform.Translation = new Vector3(10, 0, 0);

// The rotated top node will affect all child nodes
top.Transform.Rotation = Quaternion.FromEulerAngle(Math.PI, 4, 0);
          
// Save 3D scene in the supported file formats
scene.Save("NodeHierarchy.fbx");

{{< /highlight >}}
##  **Condividi i dati della geometria di Mesh tra più nodi**
Per diminuire le necessità di memoria, una singola istanza di [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Classe può essere associata a varie istanze di [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Classe. Immaginate che avete bisogno di un sistema in cui tutti i 3D cubi sembravano essere indistinguibili, tuttavia avete richiesto numerosi un gran numero di loro. È possibile risparmiare memoria creando un oggetto Mesh all'avvio del sistema. A quel punto, ogni volta che hai richiesto un'altra forma, crei un altro oggetto Node, quindi punta quel nodo a quello Mesh. Questo si chiama istanza. Aspose.3D for .NET Le API consentono di eseguire l'istanza.
###  **Esempio di installazione**
Nei giochi RTS (strategia in tempo reale) come, possiamo sempre vedere più NPC (Carattere non giocatore) con lo stesso modello 3D, forse in colori diversi, il motore di rendering di solito condivide gli stessi dati della geometria della mesh su NPC diversi, questa tecnica si chiama Installazione.

{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Dimostrazione del codice di esempio:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Define color vectors
Vector3[] colors = new Vector3[] {
new Vector3(1, 0, 0),
new Vector3(0, 1, 0),
new Vector3(0, 0, 1)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
int idx = 0;
foreach (Vector3 color in colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.Entity = mesh;
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.DiffuseColor = color;
    // Set material
    cube.Material = mat;
    // Set translation
    cube.Transform.Translation = new Vector3(idx++ * 20, 0, 0);
    // Add cube node
    scene.RootNode.ChildNodes.Add(cube);
}
        
// Save 3D scene in the supported file formats
scene.Save("MeshGeometryData.fbx");

{{< /highlight >}}

In questo esempio abbiamo creato 3 nodi cubo condividono la stessa mesh, ognuno di essi ha materiale diverso con colori diversi.
