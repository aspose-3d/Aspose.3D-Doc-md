---
title: Crea maglia e scena 3D
type: docs
weight: 10
url: /it/net/create-3d-mesh-and-scene/
description: Una mesh è definita da un insieme di punti di controllo e da molti poligoni n-sided secondo necessità. Questo articolo spiega come definire una Mesh.
---
## **Creare una maglia cubica 3D**
Un [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) è definito da un insieme di punti di controllo e da molti poligoni n-sided secondo necessità. Questo articolo spiega come definire un `Mesh`.

Per creare una superficie `Mesh`, dobbiamo definire i punti di controllo e i poligoni come segue:

- [Definire i punti di controllo](/3d/it/net/create-3d-mesh-and-scene/)
- [Creare poligoni con classe PolygonBuilder](/3d/it/net/create-3d-mesh-and-scene/)
- [Crea poligoni](/3d/it/net/create-3d-mesh-and-scene/)

Ecco un esempio per allegare un materiale Phong al nodo cubo:
### **Definire i punti di controllo**
Una mesh è composta da un insieme di punti di controllo nello spazio e poligoni per descrivere la superficie della mesh, per creare una mesh, dobbiamo definire i punti di controllo:

{{% alert color="primary" %}}

I punti di controllo di tutte le geometrie in Aspose.3D utilizzano coordinate omogenee, quindi è `Vector4` invece di Vector3 nel codice di esempio.

{{% /alert %}}

**Esempio:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-DefineControlPoints.cs" >}}


### **Crea poligoni**
I punti di controllo non sono renderabili, per rendere visibile il cubo, dobbiamo definire poligoni in ogni lato:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.cs" >}}


### **Creare poligoni con classe PolygonBuilder**
Possiamo anche definire poligono per vertici con classe `PolygonBuilder`:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.cs" >}}

Ora è finito, per rendere visibile la mesh, dobbiamo preparare un nodo per questo.
## **Come Triangolare una Mesh**
La mesh triangolata è utile per l'industria dei giochi perché il triangolare è l'unica primitiva supportata che l'hardware della GPU supporta (i dati non triangolari sono triangolati a livello di driver, il che è inefficiente nel rendering in tempo reale)

{{% alert color="primary" %}}

In questa versione abbiamo solo triangolato i poligoni poiché è richiesto dall'esportazione di file 3ds, normali/uvs e altri elementi vertici vengono persi durante questa procedura, possiamo implementarlo in futuro.

{{% /alert %}}

In questo esempio, triangoliamo una mesh importando il file FBX e lo salviamo in formato FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.cs" >}}
## **Creare una scena cubica 3D**
Questo argomento mostra come aggiungere la geometria mesh alla scena 3D. Il codice di esempio inserisce un cubo e salva la scena 3D nei formati di file supportati.
### **Creare un Nodo Cubo**
Un nodo è invisibile, ma è possibile eseguire il rendering della geometria collegata al nodo.

{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo[Creare un oggetto classe Mesh come narrato lì](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Esempio**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-CubeScene-CreateCubeScene.cs" >}}

{{% alert color="primary" %}}

NOTA: le entità associate al nodo radice vengono solitamente ignorate nei software CAD/CAM, quindi è necessario creare un nuovo nodo per eseguire il rendering della geometria.

{{% /alert %}}
