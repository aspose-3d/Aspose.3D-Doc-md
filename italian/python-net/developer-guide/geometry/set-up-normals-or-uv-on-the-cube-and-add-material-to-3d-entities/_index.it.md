---
title: Imposta normali o UV sul cubo e aggiungi materiale a 3D entità
type: docs
weight: 20
url: /it/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Come creare dati normali o uv su una mesh in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET offre la gestione di normali e UV sulle forme geometriche. Una mesh memorizza le proprietà chiave per ogni vertice sono la sua posizione nello spazio e la sua normale, un vettore perpendicolare alla superficie originale. La normalità è importante per i conteggi delle ombreggiature. I normali dovrebbero essere vettori unitari. La maggior parte dei formati mesh supporta anche una qualche forma di coordinate UV che sono una rappresentazione 2d separata della mesh "spiegata" per mostrare quale parte di una mappa texture bidimensionale applicare a diversi poligoni della mesh.

{{% /alert %}} {{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto di classe `Mesh` come narrato lì](/3d/it/python-net/create-3d-mesh-and-scene/) e quindi puntare il nodo alla geometria Mesh di [Creazione di una scena 3D](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Creare vettori normali**
Per avere un buon aspetto visivo sull'illuminazione, dobbiamo specificare le informazioni normali per ogni vertice, per avere dettagli migliori, possiamo anche usare la mappa normale e diffusa (certo che puoi usare la mappa ombra/speculare) per eseguire per pixel normale/colore. Un'informazione per vertice come il colore normale o del vertice viene ottenuta da `VertexElement`. In Aspose.3D possiamo mappare informazioni extra per controllare punti/vertice poligono/poligono/bordo, un campione per definire normali per vertice:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

Gli 8 vettori normali sono mappati direttamente a 8 punti di controllo, nell'esempio successivo, dimostreremo uno scenario un po 'più complesso.
##  **Creare coordinate UV**
Qui, abbiamo definito solo 4 coordinate UV, ma le abbiamo applicate a 24 vertici poligonali (6 vertici faccia * 4 per poligono) utilizzando indici.
Aspose.3D fornisce 5 modalità di mappatura:

- `CONTROL_POINT` -ogni dato viene mappato al punto di controllo della geometria.
- `POLYGON_VERTEX` -i dati sono mappati al vertice del poligono.
- `POLYGON` -i dati sono mappati al poligono.
- `EDGE` -i dati sono mappati al bordo.
- `ALL_SAME` -un dato mappato all'intera geometria.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
##  **Aggiungi materiali agli oggetti 3D**
Aspose.3D for Python via .NET consente agli sviluppatori di utilizzare l'algoritmo di ombreggiatura per ombreggiature e luci accurate. Il Phong ha diversi input di mappa che possiamo usare per mascherare l'effetto al nodo. Il rendering basato sulla fisica (PBR) tiene conto di alcune proprietà fisiche degli oggetti, un tale approccio fornisce l'aspetto dei materiali come nel mondo reale.
###  **Materiale Phong con texture per il cubo**
Quando le coordinate UV sono pronte per l'uso, possiamo applicare una texture sulla superficie della mesh utilizzando il materiale. Solo il colore dei vertici non può descrivere i dettagli della superficie, questo è ciò per cui i materiali utilizzati. Ecco un esempio per allegare un materiale Phong al nodo cubo:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

Abbiamo specificato la mappatura della trama diffusa e un colore speculare con un parametro di lucentezza.
###  **Applicare materiale di rendering basato sulla fisica (PBR) a una scatola**
PBR gioca un ruolo chiave per le immagini del motore di gioco, con il suo rendering efficiente e realistico delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e della dispersione della luce riflessa. Gli sviluppatori possono utilizzare Aspose.3D API per applicare materiale PBR a 3D oggetti in una scena. Questo esempio di codice mostra come creare un oggetto Box e quindi applicare il materiale PBR.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
