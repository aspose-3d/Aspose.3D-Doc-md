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

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
##  **Condividi i dati della geometria di Mesh tra più nodi**
Per diminuire le necessità di memoria, una singola istanza di `Mesh` Classe può essere associata a varie istanze di `Node` Classe. Immaginate che avete bisogno di un sistema in cui tutti i 3D cubi sembravano essere indistinguibili, tuttavia avete richiesto numerosi un gran numero di loro. È possibile risparmiare memoria creando un oggetto Mesh all'avvio del sistema. A quel punto, ogni volta che hai richiesto un'altra forma, crei un altro oggetto Nodo, quindi punta quel nodo a quello `Mesh`. Questo si chiama istanza. Aspose. Le API 3D for Java consentono di eseguire l'istanza.
###  **Esempio di installazione**
Nei giochi RTS (strategia in tempo reale) come, possiamo sempre vedere più NPC (Carattere non giocatore) con lo stesso modello 3D, forse in colori diversi, il motore di rendering di solito condivide gli stessi dati della geometria della mesh su NPC diversi, questa tecnica si chiama Installazione.

{{% alert color="primary" %}} 

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Dimostrazione del codice di esempio:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In questo esempio abbiamo creato 3 nodi cubo condividono la stessa mesh, ognuno di essi ha materiale diverso con colori diversi.
