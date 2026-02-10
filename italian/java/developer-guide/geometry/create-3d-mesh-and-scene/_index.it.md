---
title: Crea mesh e scena 3D
type: docs
weight: 40
url: /it/java/create-3d-mesh-and-scene/
description: Una mesh è definita da un insieme di punti di controllo e da molti poligoni n-sided secondo necessità. Questo articolo spiega come definire una Mesh.
---
##  **Crea una mesh cubica da 3D**
Un `Mesh` è definito da un insieme di punti di controllo e da molti poligoni n-sided, se necessario. Questo articolo spiega come definire un `Mesh`.

Per creare una superficie `Mesh`, dobbiamo definire i punti di controllo e i poligoni come segue:

- [Definire i punti di controllo](/3d/it/java/create-3d-mesh-and-scene-html/)
- [Crea poligoni con classe PolygonBuilder](/3d/it/java/create-3d-mesh-and-scene-html/)
- [Crea poligoni](/3d/it/java/create-3d-mesh-and-scene-html/)

Ecco un esempio per allegare un materiale Phong al nodo cubo:
###  **Definire i punti di controllo**
Una mesh è composta da un insieme di punti di controllo nello spazio e poligoni per descrivere la superficie della mesh, per creare una mesh, dobbiamo definire i punti di controllo:

{{% alert color="primary" %}} 

I punti di controllo di tutte le geometrie in Aspose.3D utilizzano coordinate omogenee, quindi nel codice di esempio sono `Vector4` invece di `Vector3`.

{{% /alert %}} 

**Esempio:**

{{< highlight "java" >}}
// Initialize control points
Vector4List controlPoints = new Vector4List(8);
controlPoints.add(new Vector4( -5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, -5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, -5.0, 1.0));
{{< /highlight >}}



###  **Crea poligoni**
I punti di controllo non sono renderabili, per rendere visibile il cubo, dobbiamo definire poligoni in ogni lato:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.createPolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.createPolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.createPolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.createPolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.createPolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.createPolygon(new int[] { 3, 2, 6, 7 });
{{< /highlight >}}



###  **Crea poligoni con classe PolygonBuilder**
Possiamo anche definire poligono per vertici con PolygonBuilder classe:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
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
    builder.begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.addVertex(indices[vertexId++]);
    // Finished one polygon
    builder.end();
}
{{< /highlight >}}

Ora è finito, per rendere visibile la mesh, dobbiamo preparare un nodo per questo.
##  **Come Triangolare una Mesh**
La mesh triangolata è utile per l'industria dei giochi perché il triangolare è l'unica primitiva supportata che l'hardware della GPU supporta (i dati non triangolari sono triangolati a livello di driver, il che è inefficiente nel rendering in tempo reale)

{{% alert color="primary" %}} 

In questa versione abbiamo solo triangolato i poligoni poiché è richiesto dall'esportazione di file 3ds, normali/uvs e altri elementi vertici vengono persi durante questa procedura, possiamo implementarlo in futuro.

{{% /alert %}} 

In questo esempio, triangolare una mesh importando FBX file e salvandolo in formato FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
scene.open(MyDir + "document.fbx");
scene.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            // Triangulate the mesh
            Mesh newMesh = PolygonModifier.triangulate(mesh);
            // Replace the old mesh
            node.setEntity(newMesh);
        }
        return true;
    }
});
MyDir = MyDir + RunExamples.getOutputFilePath("document.fbx");
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Crea una scena del cubo 3D**
Questo argomento mostra come aggiungere la geometria mesh alla scena 3D. Il codice di esempio inserisce un cubo e salva 3D scena nei formati di file supportati.
###  **Creare un Nodo Cubo**
Un nodo è invisibile, ma è possibile eseguire il rendering della geometria collegata al nodo.

{{% alert color="primary" %}} 

L'oggetto della classe Mesh viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Esempio:**

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("CubeScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}

{{% alert color="primary" %}} 

NOTA: le entità associate al nodo radice vengono solitamente ignorate nei software CAD/CAM, quindi è necessario creare un nuovo nodo per eseguire il rendering della geometria.

{{% /alert %}}
