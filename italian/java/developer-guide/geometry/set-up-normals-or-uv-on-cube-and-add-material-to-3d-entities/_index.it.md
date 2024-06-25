---
title: Imposta normali o UV su Cube e aggiungi materiale a 3D entità
type: docs
weight: 60
url: /it/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java offerte per gestire normali e UV sulle forme geometriche. Una mesh memorizza le proprietà della chiave per ogni vertice, la posizione nello spazio e la sua normale, nota come vettore perpendicolare alla superficie originale. La normalità è maggiore per i conteggi delle ombreggiature e dovrebbe essere un vettore unitario. La maggior parte dei formati mesh supporta anche una qualche forma di coordinate UV che sono una rappresentazione 2D separata della mesh "spiegata" per mostrare quale parte di una mappa texture bidimensionale applicare a diversi poligoni della mesh.
---
{{% alert color="primary" %}}

Aspose.3D for Java offerte per gestire normali e UV sulle forme geometriche. Una mesh memorizza le proprietà della chiave per ogni vertice, la posizione nello spazio e la sua normale, nota come vettore perpendicolare alla superficie originale. La normalità è maggiore per i conteggi delle ombreggiature e dovrebbe essere un vettore unitario. La maggior parte dei formati mesh supporta anche una qualche forma di coordinate UV che sono una rappresentazione 2D separata della mesh "spiegata" per mostrare quale parte di una mappa texture bidimensionale applicare a diversi poligoni della mesh.

{{% /alert %}} {{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato qui](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) e quindi puntare il nodo alla geometria mesh creando una scena 3D.

{{% /alert %}}
##  **Creare vettori normali**
Per avere una buona visione visiva dell'illuminazione, dobbiamo specificare le informazioni normali per ogni vertice. Per avere i dettagli migliori, possiamo anche usare la mappa normale e diffusa (usa ombra/mappa speculare) per eseguire per pixel normale/colore. Un'informazione per vertice come il colore normale o del vertice viene ottenuta da VertexElement. In Aspose.3D possiamo mappare informazioni extra per controllare punti/vertice poligono/poligono/bordo, un campione per definire normali per vertice:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


Gli 8 vettori normali sono mappati direttamente a 8 punti di controllo, nell'esempio successivo, dimostreremo uno scenario un po 'più complesso.
##  **Creare coordinate UV**
Qui, abbiamo definito solo 4 coordinate UV, ma le abbiamo applicate a 24 vertici poligonali (6 vertici faccia * 4 per poligono) utilizzando indici.
Aspose.3D fornisce 5 modalità di mappatura:

- **Punto di controllo**-Ogni dato viene mappato al punto di controllo della geometria.
- **Poligonvertex**-I dati sono mappati al vertice del poligono.
- **Poligono**-I dati sono mappati al poligono.
- **Bordo**-I dati sono mappati al bordo.
- **AllSame**-Un dato mappato all'intera geometria.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
##  **Aggiungi materiali agli oggetti 3D**
Aspose.3D for Java consente agli sviluppatori di utilizzare l'algoritmo di ombreggiatura per ombreggiature e luci accurate. Il Phong ha diversi input di mappa che possiamo usare per mascherare l'effetto al nodo. Il rendering basato sulla fisica (PBR) tiene conto di alcune proprietà fisiche degli oggetti, un tale approccio fornisce l'aspetto dei materiali come nel mondo reale.
###  **Materiale Phong con texture per il cubo**
Quando le coordinate UV sono pronte per l'uso, possiamo applicare una texture sulla superficie della mesh utilizzando il materiale. Solo il colore dei vertici non può descrivere i dettagli della superficie, questo è ciò per cui i materiali utilizzati. Ecco un esempio per allegare un materiale Phong al nodo cubo:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


Abbiamo specificato la mappatura della trama diffusa e un colore speculare con un parametro di lucentezza.
###  **Applicare materiale di rendering basato sulla fisica (PBR) a una scatola**
PBR gioca un ruolo chiave per le immagini del motore di gioco, con il suo rendering efficiente e realistico delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e della dispersione della luce riflessa. Gli sviluppatori possono utilizzare Aspose.3D API per applicare materiale PBR a 3D oggetti in una scena. Questo esempio di codice mostra come creare un oggetto Box e quindi applicare il materiale PBR.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
