---
title: Lägg till nodehierarki och Dela geometriska data av mesh bland flera noder i 3D Scene
type: docs
weight: 40
url: /sv/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
---
##  **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D for .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
###  **Exempel**
En provscen hierarki ser ut som:

![todo:image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

I Aspose. 3D, kan varje `Node` instans ha flera barnnoder, i detta exempel skapade vi en nod med två kubnoder, Om vi roterar rotnoden, alla barnnoder påverkas också:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Get a child node object
Node top = scene.RootNode.CreateChildNode();
// Each cube node has their own translation
Node cube1 = top.CreateChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();            
// Point node to the mesh
cube1.Entity = mesh;
// Set first cube translation
cube1.Transform.Translation = new Vector3(-10, 0, 0);
Node cube2 = top.CreateChildNode("cube2");
// Point node to the mesh
cube2.Entity = mesh;
// Set second cube translation
cube2.Transform.Translation = new Vector3(10, 0, 0);

// The rotated top node will affect all child nodes
top.Transform.Rotation = Quaternion.FromEulerAngle(Math.PI, 4, 0);
          
// Save 3D scene in the supported file formats
scene.Save("NodeHierarchy.fbx");

{{< /highlight >}}
##  **Dela meshs geometri data mellan flera noder**
För att minska minnesförnödenheter, kan en enda instans av [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) klass bindas till olika instanser av [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara oundvikliga, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, du gör en annan Node objekt, sedan peka den noden till en Mesh. Detta kallas instanser. Aspose.3D for .NET API tillåter att göra instanser.
###  **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, renderingsmotorn brukar dela samma data för mashgeometri med olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration av exempelkod:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Define color vectors
Vector3[] colors = new Vector3[] {
new Vector3(1, 0, 0),
new Vector3(0, 1, 0),
new Vector3(0, 0, 1)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
int idx = 0;
foreach (Vector3 color in colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.Entity = mesh;
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.DiffuseColor = color;
    // Set material
    cube.Material = mat;
    // Set translation
    cube.Transform.Translation = new Vector3(idx++ * 20, 0, 0);
    // Add cube node
    scene.RootNode.ChildNodes.Add(cube);
}
        
// Save 3D scene in the supported file formats
scene.Save("MeshGeometryData.fbx");

{{< /highlight >}}

I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
