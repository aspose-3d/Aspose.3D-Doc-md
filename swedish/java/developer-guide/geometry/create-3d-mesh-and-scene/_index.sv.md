---
title: Skapa 3D Mesh och Scene
type: docs
weight: 40
url: /sv/java/create-3d-mesh-and-scene/
description: En Mesh definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.
---
##  **Skapa en 3D kubst**
En `Mesh` definieras av en uppsättning kontrollpunkter och de många polygoner som behövs. Den här artikeln förklarar hur man definierar en `Mesh`.

För att skapa en `Mesh`-yta måste vi definiera styrpunkter och polygoner på följande sätt:

- [Define the Control Points](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons with PolygonBuilder Class](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons](/3d/java/create-3d-mesh-and-scene-html/)

Här är ett exempel för att bifoga ett Phong-material till kubennoden:
###  **Definiera kontrollpunkter**
En mash består av en uppsättning styrpunkter i rymden och polygoner för att beskriva maskstytan för att skapa en mask. Vi måste definiera kontrollpunkterna:

{{% alert color="primary" %}} 

Kontrollpunkterna för alla geometrier i Aspose. 3D använd homogen koordinat, så det är `Vector4` istället för `Vector3` i exempelkoden.

{{% /alert %}} 

**Exempel:**

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



###  **Skapa polygoner**
Kontrollpunkterna är inte utförbara, för att göra kuben synlig, måste vi definiera polygoner i varje sida:

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



###  **Skapa polygoner med PolygonBuilder Name**
Vi kan också definiera polygon med hörn med PolygonBuilder klass:

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

Nu är det klart, för att göra nätverket synligt, måste vi förbereda en nod för det.
##  **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds GPU-hårdvaran stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering)

{{% alert color="primary" %}} 

I denna version vi bara triangulerade polygoner eftersom det krävs av 3ds fil export, normaler/uvs och andra vertex element går förlorade under denna förfarande, vi kan genomföra detta i framtiden.

{{% /alert %}} 

I det här exemplet triangulerar vi en mesh genom att importera FBX-fil och sparade den i FBX-format.

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
##  **Skapa en 3D kubscene**
Detta ämne visar hur mesh-geometrin ska läggas till i 3D-scenen. Exemplets kod placerar en kub och sparar 3D scen i de filformat som stöds.
###  **Skapa en kubnod**
En nod är osynlig, men geometrin som är kopplad till noden kan renderas.

{{% alert color="primary" %}} 

Mesh-klassobjektet används i koden. Vi kan [Skapa ett Mesh-klassobjekt som berättat där.](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Exempel:**

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

OBS: De enheter som är anslutna till rotnoden ignoreras vanligtvis i CAD/CAM-programvara, så vi behöver skapa en ny nod för att göra geometrin.

{{% /alert %}}
