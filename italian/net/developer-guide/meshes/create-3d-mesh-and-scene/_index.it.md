---
title: Crea mesh e scena 3D
type: docs
weight: 10
url: /it/net/create-3d-mesh-and-scene/
description: Una mesh è definita da un insieme di punti di controllo e da molti poligoni n-sided secondo necessità. Questo articolo spiega come definire una Mesh.
---
##  **Crea una mesh cubica da 3D**
Un [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) è definito da un insieme di punti di controllo e da molti poligoni n-sided, se necessario. Questo articolo spiega come definire un `Mesh`.

Per creare una superficie `Mesh`, dobbiamo definire i punti di controllo e i poligoni come segue:

- [Definire i punti di controllo](/3d/it/net/create-3d-mesh-and-scene/)
- [Crea poligoni con classe PolygonBuilder](/3d/it/net/create-3d-mesh-and-scene/)
- [Crea poligoni](/3d/it/net/create-3d-mesh-and-scene/)

Ecco un esempio per allegare un materiale Phong al nodo cubo:
###  **Definire i punti di controllo**
Una mesh è composta da un insieme di punti di controllo nello spazio e poligoni per descrivere la superficie della mesh, per creare una mesh, dobbiamo definire i punti di controllo:

{{% alert color="primary" %}}

I punti di controllo di tutte le geometrie in Aspose.3D utilizzano coordinate omogenee, quindi è `Vector4` invece di Vector3 nel codice di esempio.

{{% /alert %}}

**Esempio:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize control points
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};

{{< /highlight >}}


###  **Crea poligoni**
I punti di controllo non sono renderabili, per rendere visibile il cubo, dobbiamo definire poligoni in ogni lato:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Vector4[] controlPoints = DefineControlPoints();
            
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.ControlPoints.AddRange(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.CreatePolygon(new int[] { 3, 2, 6, 7 });

{{< /highlight >}}


###  **Crea poligoni con classe PolygonBuilder**
Possiamo anche definire poligono per vertici con `PolygonBuilder` classe:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Vector4[] controlPoints = DefineControlPoints();
            
// Initialize mesh object
Mesh mesh = new Mesh();

// Add control points to the mesh
mesh.ControlPoints.AddRange(controlPoints);
            
// Indices of the vertices per each polygon
int[] indices = new int[]
{
    0,1,2,3, // Front face (Z+)
    1,5,6,2, // Right side (X+)
    5,4,7,6, // Back face (Z-)
    4,0,3,7, // Left side (X-)
    0,4,5,1, // Bottom face (Y-)
    3,2,6,7 // Top face (Y+)
};

int vertexId = 0;
PolygonBuilder builder = new PolygonBuilder(mesh);
for (int face = 0; face < 6; face++)
{
    // Start defining a new polygon
    builder.Begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.AddVertex(indices[vertexId++]);
    // Finished one polygon
    builder.End();
}


{{< /highlight >}}

Ora è finito, per rendere visibile la mesh, dobbiamo preparare un nodo per questo.
##  **Come Triangolare una Mesh**
La mesh triangolata è utile per l'industria dei giochi perché il triangolare è l'unica primitiva supportata che l'hardware della GPU supporta (i dati non triangolari sono triangolati a livello di driver, il che è inefficiente nel rendering in tempo reale)

{{% alert color="primary" %}}

In questa versione abbiamo solo triangolato i poligoni poiché è richiesto dall'esportazione di file 3ds, normali/uvs e altri elementi vertici vengono persi durante questa procedura, possiamo implementarlo in futuro.

{{% /alert %}}

In questo esempio, triangolare una mesh importando FBX file e salvandolo in formato FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
           
// Initialize scene object
Scene scene = Scene.FromFile("document.fbx");
            
scene.RootNode.Accept(delegate(Node node)
{
    Mesh mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        // Triangulate the mesh
        Mesh newMesh = PolygonModifier.Triangulate(mesh);
        // Replace the old mesh
        node.Entity = mesh;
    }
    return true;
});
scene.Save("document.fbx");

{{< /highlight >}}
##  **Crea una scena del cubo 3D**
Questo argomento mostra come aggiungere la geometria mesh alla scena 3D. Il codice di esempio inserisce un cubo e salva 3D scena nei formati di file supportati.
###  **Creare un Nodo Cubo**
Un nodo è invisibile, ma è possibile eseguire il rendering della geometria collegata al nodo.

{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Esempio**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();           

// Point node to the Mesh geometry
cubeNode.Entity = mesh;
            
// Add Node to a scene
scene.RootNode.ChildNodes.Add(cubeNode);           

// Save 3D scene in the supported file formats
scene.Save("CubeScene.fbx");           

{{< /highlight >}}

{{% alert color="primary" %}}

NOTA: le entità associate al nodo radice vengono solitamente ignorate nei software CAD/CAM, quindi è necessario creare un nuovo nodo per eseguire il rendering della geometria.

{{% /alert %}}
