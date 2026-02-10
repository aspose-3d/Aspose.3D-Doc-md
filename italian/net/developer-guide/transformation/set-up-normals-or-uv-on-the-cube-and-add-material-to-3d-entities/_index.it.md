---
title: Imposta normali o UV sul cubo e aggiungi materiale a 3D entità
type: docs
weight: 20
url: /it/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Come creare dati normali o uv su una mesh in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET offerte per gestire normali e UV sulle forme geometriche. Una mesh memorizza le proprietà chiave per ogni vertice sono la sua posizione nello spazio e la sua normale, un vettore perpendicolare alla superficie originale. La normalità è importante per i conteggi delle ombreggiature. I normali dovrebbero essere vettori unitari. La maggior parte dei formati mesh supporta anche una qualche forma di coordinate UV che sono una rappresentazione 2d separata della mesh "spiegata" per mostrare quale parte di una mappa texture bidimensionale applicare a diversi poligoni della mesh.

{{% /alert %}} {{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](/3d/it/net/create-3d-mesh-and-scene/) e quindi puntare il nodo alla geometria Mesh di [Creazione di una scena 3D](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Creare vettori normali**
Per avere un buon aspetto visivo sull'illuminazione, dobbiamo specificare le informazioni normali per ogni vertice, per avere dettagli migliori, possiamo anche usare la mappa normale e diffusa (certo che puoi usare la mappa ombra/speculare) per eseguire per pixel normale/colore. Un'informazione per vertice come il colore normale o del vertice viene ottenuta da VertexElement. In Aspose.3D possiamo mappare informazioni extra per controllare punti/vertice poligono/poligono/bordo, un campione per definire normali per vertice:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;
// Copy the data to the vertex element
elementNormal.Data.AddRange(normals);

{{< /highlight >}}

Gli 8 vettori normali sono mappati direttamente a 8 punti di controllo, nell'esempio successivo, dimostreremo uno scenario un po 'più complesso.
##  **Creare coordinate UV**
Qui, abbiamo definito solo 4 coordinate UV, ma le abbiamo applicate a 24 vertici poligonali (6 vertici faccia * 4 per poligono) utilizzando indici.
Aspose.3D fornisce 5 modalità di mappatura:

- `ControlPoint` -ogni dato viene mappato al punto di controllo della geometria.
- `PolygonVertex` -i dati sono mappati al vertice del poligono.
- `Polygon` -i dati sono mappati al poligono.
- `Edge` -i dati sono mappati al bordo.
- `AllSame` -un dato mappato all'intera geometria.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();

// Create UVset
VertexElementUV elementUV = mesh.CreateElementUV(TextureMapping.Diffuse, MappingMode.PolygonVertex, ReferenceMode.IndexToDirect);
// Copy the data to the UV vertex element 
elementUV.Data.AddRange(uvs);
elementUV.Indices.AddRange(uvsId);

{{< /highlight >}}
##  **Aggiungi materiali agli oggetti 3D**
Aspose.3D for .NET consente agli sviluppatori di utilizzare l'algoritmo di ombreggiatura per ombreggiature e luci accurate. Il Phong ha diversi input di mappa che possiamo usare per mascherare l'effetto al nodo. Il rendering basato sulla fisica (PBR) tiene conto di alcune proprietà fisiche degli oggetti, un tale approccio fornisce l'aspetto dei materiali come nel mondo reale.
###  **Materiale Phong con texture per il cubo**
Quando le coordinate UV sono pronte per l'uso, possiamo applicare una texture sulla superficie della mesh utilizzando il materiale. Solo il colore dei vertici non può descrivere i dettagli della superficie, questo è ciò per cui i materiali utilizzati. Ecco un esempio per allegare un materiale Phong al nodo cubo:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize cube node object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
         
// Point node to the mesh
cubeNode.Entity = mesh;
            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);
            
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
            
// Initiallize Texture object
Texture diffuse = new Texture();
            
// The path to the documents directory.
            
// Set local file path
diffuse.FileName = RunExamples.GetOutputFilePath("surface.dds");

// Set Texture of the material
mat.SetTexture("DiffuseColor", diffuse);

// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.FileName = "embedded-texture.png";
// Set binary content
diffuse.Content = File.ReadAllBytes(RunExamples.GetDataFilePath("aspose-logo.jpg"));

// Set color
mat.SpecularColor = new Vector3(Color.Red);

// Set brightness
mat.Shininess = 100;

// Set material property of the cube object
cubeNode.Material = mat;
            
// Save 3D scene in the supported file formats
scene.Save("MaterialToCube.fbx");

{{< /highlight >}}

Abbiamo specificato la mappatura della trama diffusa e un colore speculare con un parametro di lucentezza.
###  **Applicare materiale di rendering basato sulla fisica (PBR) a una scatola**
PBR gioca un ruolo chiave per le immagini del motore di gioco, con il suo rendering efficiente e realistico delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e della dispersione della luce riflessa. Gli sviluppatori possono utilizzare Aspose.3D API per applicare materiale PBR a 3D oggetti in una scena. Questo esempio di codice mostra come creare un oggetto Box e quindi applicare il materiale PBR.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
