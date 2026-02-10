---
title: Skapa 3D Mesh och Scene
type: docs
weight: 10
url: /sv/net/create-3d-mesh-and-scene/
description: En Mesh definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.
---
##  **Skapa en 3D kubst**
En [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) definieras av en uppsättning kontrollpunkter och de många polygoner som behövs. Den här artikeln förklarar hur man definierar en `Mesh`.

För att skapa en `Mesh`-yta måste vi definiera styrpunkter och polygoner på följande sätt:

- [Define the Control Points](/3d/net/create-3d-mesh-and-scene/)
- [Create Polygons with PolygonBuilder Class](/3d/net/create-3d-mesh-and-scene/)
- [Create Polygons](/3d/net/create-3d-mesh-and-scene/)

Här är ett exempel för att bifoga ett Phong-material till kubennoden:
###  **Definiera kontrollpunkter**
En mash består av en uppsättning styrpunkter i rymden och polygoner för att beskriva maskstytan för att skapa en mask. Vi måste definiera kontrollpunkterna:

{{% alert color="primary" %}}

Kontrollpunkterna för alla geometrier i Aspose. 3D använd homogen koordinat, så det är `Vector4` istället för Vector3 i exempelkoden.

{{% /alert %}}

**Exempel:**

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


###  **Skapa polygoner**
Kontrollpunkterna är inte utförbara, för att göra kuben synlig, måste vi definiera polygoner i varje sida:

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


###  **Skapa polygoner med PolygonBuilder Name**
Vi kan också definiera polygon med hörn med `PolygonBuilder` klass:

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

Nu är det klart, för att göra nätverket synligt, måste vi förbereda en nod för det.
##  **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds GPU-hårdvaran stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering)

{{% alert color="primary" %}}

I denna version vi bara triangulerade polygoner eftersom det krävs av 3ds fil export, normaler/uvs och andra vertex element går förlorade under denna förfarande, vi kan genomföra detta i framtiden.

{{% /alert %}}

I det här exemplet triangulerar vi en mesh genom att importera FBX-fil och sparade den i FBX-format.

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
##  **Skapa en 3D kubscene**
Detta ämne visar hur mesh-geometrin ska läggas till i 3D-scenen. Exemplets kod placerar en kub och sparar 3D scen i de filformat som stöds.
###  **Skapa en kubnod**
En nod är osynlig, men geometrin som är kopplad till noden kan renderas.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Exempel**

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

OBS: De enheter som är anslutna till rotnoden ignoreras vanligtvis i CAD/CAM-programvara, så vi behöver skapa en ny nod för att göra geometrin.

{{% /alert %}}
