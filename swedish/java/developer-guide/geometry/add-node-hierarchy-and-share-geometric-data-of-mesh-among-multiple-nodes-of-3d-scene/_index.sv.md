---
title: Lägg till nodehierarki och Dela geometriska data av mesh bland flera noder i 3D Scene
type: docs
weight: 20
url: /sv/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java har stöd för att bygga en hierarki av noder. Noden är grundläggande byggsten för 3D scen och en hierarki av noder definierar den logiska strukturen i 3D scener Denna förordning träder i kraft dagen efter det att den har offentliggjorts i Europeiska unionens officiella tidning. och ge synligt innehåll genom att fästa geometrier, ljus och kameror till noder.
---
##  **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D for Java har stöd för att bygga en hierarki av noder. `Node` är grundläggande byggsten för 3D scen och en hierarki av noder definierar den logiska strukturen för 3D Scenen. och ge synligt innehåll genom att fästa geometrier, ljus och kameror till noder.
###  **Exempel**

I Aspose. 3D, kan varje `Node` instans ha flera barnnoder, i detta exempel skapade vi en nod med två kubnoder, Om vi roterar rotnoden, alla barnnoder påverkas också:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node top = scene.getRootNode().createChildNode();
// Each cube node has their own translation
Node cube1 = top.createChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cube1.setEntity(mesh);
// Set first cube translation
cube1.getTransform().setTranslation(new Vector3(-10, 0, 0));
Node cube2 = top.createChildNode("cube2");
// Point node to the mesh
cube2.setEntity(mesh);
// Set second cube translation
cube2.getTransform().setTranslation(new Vector3(10, 0, 0));
// The rotated top node will affect all child nodes
top.getTransform().setRotation(Quaternion.fromEulerAngle(Math.PI, 4, 0));
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("NodeHierarchy.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Dela meshs geometri data mellan flera noder**
För att minska minnesförnödenheter, kan en enda instans av `Mesh` klass bindas till olika instanser av `Node` klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara oundvikliga, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, gör du ett annat Node objekt, sedan peka den noden till en `Mesh`. Detta kallas instanser. Aspose.3D for Java API tillåter att göra instanser.
###  **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, renderingsmotorn brukar dela samma data för mashgeometri med olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demonstration av exempelkod:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Define color vectors
Vector3[] colors = new Vector3[] {
    new Vector3(1, 0, 0),
    new Vector3(0, 1, 0),
    new Vector3(0, 0, 1)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
int idx = 0;
for(Vector3 color : colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.setEntity(mesh);
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.setDiffuseColor(color);
    // Set material
    cube.setMaterial(mat);
    // Set translation
    cube.getTransform().setTranslation(new Vector3(idx++ * 20, 0, 0));
    // Add cube node
    scene.getRootNode().addChildNode(cube);
}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("MeshGeometryData.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
