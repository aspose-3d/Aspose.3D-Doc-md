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

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}


Gli 8 vettori normali sono mappati direttamente a 8 punti di controllo, nell'esempio successivo, dimostreremo uno scenario un po 'più complesso.
##  **Creare coordinate UV**
Qui, abbiamo definito solo 4 coordinate UV, ma le abbiamo applicate a 24 vertici poligonali (6 vertici faccia * 4 per poligono) utilizzando indici.
Aspose.3D fornisce 5 modalità di mappatura:

- **Punto di controllo**-Ogni dato viene mappato al punto di controllo della geometria.
- **Poligonvertex**-I dati sono mappati al vertice del poligono.
- **Poligono**-I dati sono mappati al poligono.
- **Bordo**-I dati sono mappati al bordo.
- **AllSame**-Un dato mappato all'intera geometria.



{{< highlight "java" >}}
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};
// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Create UVset
VertexElementUV elementUV = mesh.createElementUV(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT);
// Copy the data to the UV vertex element
elementUV.setData(uvs);
elementUV.setIndices(uvsId);
{{< /highlight >}}
##  **Aggiungi materiali agli oggetti 3D**
Aspose.3D for Java consente agli sviluppatori di utilizzare l'algoritmo di ombreggiatura per ombreggiature e luci accurate. Il Phong ha diversi input di mappa che possiamo usare per mascherare l'effetto al nodo. Il rendering basato sulla fisica (PBR) tiene conto di alcune proprietà fisiche degli oggetti, un tale approccio fornisce l'aspetto dei materiali come nel mondo reale.
###  **Materiale Phong con texture per il cubo**
Quando le coordinate UV sono pronte per l'uso, possiamo applicare una texture sulla superficie della mesh utilizzando il materiale. Solo il colore dei vertici non può descrivere i dettagli della superficie, questo è ciò per cui i materiali utilizzati. Ecco un esempio per allegare un materiale Phong al nodo cubo:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize cube node object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cubeNode.setEntity(mesh);
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
// Initiallize Texture object
Texture diffuse = new Texture();
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Set local file path
diffuse.setFileName(MyDir + "surface.dds");
// Set Texture of the material
mat.setTexture(Material.MAP_DIFFUSE, diffuse);
// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.setFileName("embedded-texture.png");
// Set binary content
diffuse.setContent(Files.readAllBytes(Paths.get(MyDir, "aspose-logo.jpg")));
// Set color
mat.setSpecularColor(new Vector3(1, 0, 0));
// Set brightness
mat.setShininess(100);
// Set material property of the cube object
cubeNode.setMaterial(mat);
MyDir = MyDir + RunExamples.getOutputFilePath("MaterialToCube.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


Abbiamo specificato la mappatura della trama diffusa e un colore speculare con un parametro di lucentezza.
###  **Applicare materiale di rendering basato sulla fisica (PBR) a una scatola**
PBR gioca un ruolo chiave per le immagini del motore di gioco, con il suo rendering efficiente e realistico delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e della dispersione della luce riflessa. Gli sviluppatori possono utilizzare Aspose.3D API per applicare materiale PBR a 3D oggetti in una scena. Questo esempio di codice mostra come creare un oggetto Box e quindi applicare il materiale PBR.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}
