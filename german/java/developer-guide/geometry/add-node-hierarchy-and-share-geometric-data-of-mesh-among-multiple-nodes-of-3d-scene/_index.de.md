---
title: Fügen Sie Knoten hierarchie hinzu und teilen Sie geometrische Daten von Mesh unter mehreren Knoten der 3D-Szene
type: docs
weight: 20
url: /de/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java unterstützt den Aufbau einer Hierarchie von Knoten. Der Knoten ist ein grundlegender Baustein der 3D-Szene, und eine Knoten hierarchie definiert die logische Struktur der 3D-Szene und bietet sichtbaren Inhalt, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
---
##  **Knoten hierarchie in 3D Szenen dokument hinzufügen**
Aspose.3D for Java unterstützt den Aufbau einer Hierarchie von Knoten. Der `Node` ist ein grundlegender Baustein der 3D-Szene. Eine Knoten hierarchie definiert die logische Struktur der 3D-Szene und bietet sichtbaren Inhalt, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
###  **Szenen-Grafik-Beispiel**

In Aspose.3D kann jede `Node`-Instanz mehrere unter geordnete Knoten haben. In diesem Beispiel haben wir einen Knoten mit zwei Würfel knoten erstellt. Wenn wir den Stamm knoten drehen, sind auch alle unter geordneten Knoten betroffen:

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
##  **Teilen Sie die Geometrie daten von Mesh zwischen mehreren Knoten**
Um den Speicher bedarf zu verringern, kann eine einzelne Instanz der `Mesh`-Klasse an verschiedene Instanzen der `Node`-Klasse gebunden werden. Stellen Sie sich vor, dass Sie ein System benötigen, in dem alle 3D Würfel nicht zu unterscheiden schienen, aber Sie benötigten zahlreiche viele davon. Sie können Speicher platz sparen, indem Sie ein Mesh-Objekt erstellen, wenn das System gestartet wird. Zu diesem Zeitpunkt erstellen Sie jedes Mal, wenn Sie eine andere Form benötigen, ein weiteres Knoten objekt und zeigen diesen Knoten auf das Knoten `Mesh`. Dies wird als Instancing bezeichnet. Aspose.3D for Java APIs erlauben Instancing.
###  **Instancing Beispiel**
In den RTS-Spielen (Echtzeit strategie) wie können wir immer mehrere NPCs (Non-Player Character) mit demselben 3D-Modell sehen, möglicher weise in verschiedenen Farben. Die Rendering-Engine teilt normaler weise dieselben Mesh-Geometrie-Daten über verschiedene NPCs hinweg wird Instancing genannt.

{{% alert color="primary" %}} 

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demonstration des Beispiel codes:

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


In diesem Beispiel haben wir 3 Würfel knoten erstellt, die dasselbe Netz haben. Jeder von ihnen hat unterschied liches Material mit unterschied lichen Farben.
