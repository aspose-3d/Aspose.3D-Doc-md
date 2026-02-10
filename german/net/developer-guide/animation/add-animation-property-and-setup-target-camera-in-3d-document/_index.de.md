---
title: Hinzufügen von Animations eigenschaft und Setup-Ziel kamera in einem 3D-Dokument
type: docs
weight: 10
url: /de/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: In Aspose.3D ist Objekt animation eigentlich eine Key-Frame-Animation, die auf Eigenschaften animiert. Um Eigenschaften zu animieren, benötigen Sie eine CurveMapping-Instanz, die Komponenten einer Eigenschaft verschiedenen Kurven zuordnet. Beispiels weise kann eine Vector3-Eigenschaft 3 Komponenten X/Y/Z enthalten, wodurch drei Kanäle in Curve Mapping eingerichtet werden. Jeder Kanal kann einen Satz haben von Kurven.
---
##  **Animation-Eigenschaft in 3D-Dokument hinzufügen**
Aspose.3D for .NET unterstützt das Rendern animierter Szene. In diesem Artikel werden die Voraussetzungen zum Verschieben eines Objekts erläutert.
###  **Bewegen Sie die Position des Würfels**
{{% alert color="primary" %}}

Das [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](/3d/de/net/create-and-read-an-existing-3d-scene/) und es muss auch die lokale Übersetzungs eigenschaft des Knotens animieren: [Hinzufügen der Transformation zum Knoten](/3d/de/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D ist Objekt animation eigentlich eine Key-Frame-Animation, die auf Eigenschaften animiert. Um Eigenschaften zu animieren, benötigen Sie eine `CurveMapping`-Instanz, die Komponenten einer Eigenschaft verschiedenen Kurven zuordnet. Beispiels weise kann eine `Vector3`-Eigenschaft 3 Komponenten haben. `X`/`Y`/`Z`. Das wird drei Kanäle in `CurveMapping` einrichten, jeder Kanal kann einen Satz von `Curve` haben.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();             

// Each cube node has their own translation
Node cube1 = scene.RootNode.CreateChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.Transform.FindProperty("Translation");
            
// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale 
bindPoint.BindKeyframeSequence("X", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, 20.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 30.0f, Interpolation.Linear},
});

// Create the animation curve on Z component of the scale 
bindPoint.BindKeyframeSequence("Z", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, -10.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 0.0f, Interpolation.Linear},
});

// Save 3D scene in the supported file formats
scene.Save("PropertyToDocument.fbx");

{{< /highlight >}}
##  **Richten Sie die Ziel kamera in 3D-Datei ein**
Aspose.3D for .NET bietet an, die Ziel kamera in 3D-Datei einzurichten. In einigen Dateiformaten unterstützt Licht/Kamera das Ziel, wodurch das Licht/die Kamera immer einem bestimmten Knoten zugewandt ist. Dies ist in der Animation nützlich.

{{% alert color="primary" %}}

Die Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) und [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) werden im Code verwendet. Um eine `Scene`-, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode zu speichern, wird ein Dateiname mit vollständigem Pfad und [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat)-Parameter akzeptiert.

{{% /alert %}}

Im folgenden Beispiel wird das Ziel und die Kamera in der 3D-Datei eingerichtet:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
// Set camera node translation
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity<Camera>().Target = scene.RootNode.CreateChildNode("target");
scene.Save("camera-test.3ds");

{{< /highlight >}}
