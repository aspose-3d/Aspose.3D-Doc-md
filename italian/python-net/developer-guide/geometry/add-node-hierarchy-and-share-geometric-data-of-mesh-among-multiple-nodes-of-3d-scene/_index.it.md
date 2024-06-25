---
title: Aggiungi la gerarchia dei nodi e condividi i dati geometrici della mesh tra più nodi della scena 3D
type: docs
weight: 40
url: /it/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET offre la creazione di una gerarchia di nodi. Il Nodo è l'elemento costitutivo di base di una scena. Una gerarchia di nodi definisce la struttura logica di una scena e fornisce contenuto visibile collegando geometrie, luci e telecamere ai nodi.
---
##  **Aggiungi la gerarchia dei nodi nel documento della scena 3D**
Aspose.3D for Python via .NET offre la creazione di una gerarchia di nodi. Il Nodo è l'elemento costitutivo di base di una scena. Una gerarchia di nodi definisce la struttura logica di una scena e fornisce contenuto visibile collegando geometrie, luci e telecamere ai nodi.
###  **Esempio di grafico della scena**
Una gerarchia di scene campione assomiglia a:

! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D, ogni istanza `Node` può avere più nodi figlio, in questo esempio, abbiamo creato un nodo con due nodi cubo, se ruotiamo il nodo radice, anche tutti i nodi figlio vengono interessati:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
##  **Condividi i dati della geometria di Mesh tra più nodi**
Per diminuire le necessità di memoria, una singola istanza di [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Classe può essere associata a varie istanze di [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Classe. Immaginate che avete bisogno di un sistema in cui tutti i 3D cubi sembravano essere indistinguibili, tuttavia avete richiesto numerosi un gran numero di loro. È possibile risparmiare memoria creando un oggetto Mesh all'avvio del sistema. A quel punto, ogni volta che hai richiesto un'altra forma, crei un altro oggetto Node, quindi punta quel nodo a quello Mesh. Questo si chiama istanza. Le API di Aspose.3D for Python via .NET consentono di eseguire l'istanza.
###  **Esempio di installazione**
Nei giochi RTS (strategia in tempo reale) come, possiamo sempre vedere più NPC (Carattere non giocatore) con lo stesso modello 3D, forse in colori diversi, il motore di rendering di solito condivide gli stessi dati della geometria della mesh su NPC diversi, questa tecnica si chiama Installazione.

{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto di classe `Mesh` come narrato lì](/3d/it/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Dimostrazione del codice di esempio:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

In questo esempio abbiamo creato 3 nodi cubo condividono la stessa mesh, ognuno di essi ha materiale diverso con colori diversi.
