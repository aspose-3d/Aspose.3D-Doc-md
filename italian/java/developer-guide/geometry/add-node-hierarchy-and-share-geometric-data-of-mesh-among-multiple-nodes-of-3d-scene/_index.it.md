---
title: Aggiungi la gerarchia dei nodi e condividi i dati geometrici della mesh tra più nodi della scena 3D
type: docs
weight: 20
url: /it/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java supporta la creazione di una gerarchia di Nodi. Il nodo è un elemento costitutivo di base della scena 3D e una gerarchia di nodi definisce la struttura logica della scena 3D e fornisce contenuti visibili collegando geometrie, luci e telecamere ai nodi.
---
##  **Aggiungi la gerarchia dei nodi nel documento della scena 3D**
Aspose.3D for Java supporta la creazione di una gerarchia di Nodi. Il `Node` è un elemento costitutivo di base della scena 3D e una gerarchia di nodi definisce la struttura logica della scena 3D e fornisce contenuti visibili collegando geometrie, luci e telecamere ai nodi.
###  **Esempio di grafico della scena**

In Aspose.3D, ogni istanza `Node` può avere più nodi figlio, in questo esempio, abbiamo creato un nodo con due nodi cubo, se ruotiamo il nodo radice, anche tutti i nodi figlio vengono interessati:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node top = scene.getRootNode().createChildNode();
// Each cube node has their own translation
Node cube1 = top.createChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cube1.setEntity(mesh);
// Set first cube translation
cube1.getTransform().setTranslation(new Vector3(-10, 0, 0));
Node cube2 = top.createChildNode("cube2");
// Point node to the mesh
cube2.setEntity(mesh);
// Set second cube translation
cube2.getTransform().setTranslation(new Vector3(10, 0, 0));
// The rotated top node will affect all child nodes
top.getTransform().setRotation(Quaternion.fromEulerAngle(Math.PI, 4, 0));
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("NodeHierarchy.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Condividi i dati della geometria di Mesh tra più nodi**
Per diminuire le necessità di memoria, una singola istanza di `Mesh` Classe può essere associata a varie istanze di `Node` Classe. Immaginate che avete bisogno di un sistema in cui tutti i 3D cubi sembravano essere indistinguibili, tuttavia avete richiesto numerosi un gran numero di loro. È possibile risparmiare memoria creando un oggetto Mesh all'avvio del sistema. A quel punto, ogni volta che hai richiesto un'altra forma, crei un altro oggetto Nodo, quindi punta quel nodo a quello `Mesh`. Questo si chiama istanza. Aspose. Le API 3D for Java consentono di eseguire l'istanza.
###  **Esempio di installazione**
Nei giochi RTS (strategia in tempo reale) come, possiamo sempre vedere più NPC (Carattere non giocatore) con lo stesso modello 3D, forse in colori diversi, il motore di rendering di solito condivide gli stessi dati della geometria della mesh su NPC diversi, questa tecnica si chiama Installazione.

{{% alert color="primary" %}} 

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Dimostrazione del codice di esempio:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Define color vectors
Vector3[] colors = new Vector3[] {
    new Vector3(1, 0, 0),
    new Vector3(0, 1, 0),
    new Vector3(0, 0, 1)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
int idx = 0;
for(Vector3 color : colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.setEntity(mesh);
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.setDiffuseColor(color);
    // Set material
    cube.setMaterial(mat);
    // Set translation
    cube.getTransform().setTranslation(new Vector3(idx++ * 20, 0, 0));
    // Add cube node
    scene.getRootNode().addChildNode(cube);
}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("MeshGeometryData.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


In questo esempio abbiamo creato 3 nodi cubo condividono la stessa mesh, ognuno di essi ha materiale diverso con colori diversi.
