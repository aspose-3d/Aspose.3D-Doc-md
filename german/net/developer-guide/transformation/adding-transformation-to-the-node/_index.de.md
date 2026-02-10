---
title: Transformation zum Knoten hinzufügen
type: docs
weight: 30
url: /de/net/adding-transformation-to-the-node/
description: TSR (Translation/Skalierung/Rotation) werden am häufigsten im 3D-Szenario verwendet. Wir haben eine Klasse Transform bereit gestellt, um auf diese in Aspose.3D zuzugreifen.
---
{{% alert color="primary" %}}

Aspose.3D for .NET bietet an, Objekte in 3D Raum zu drehen. Es gibt drei Möglichkeiten, die Rotation des Objekts im 3D-Raum, Euler winkeln, Quaternion und Custom Matrix zu definieren. Alle werden von der [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform)-Klasse unterstützt.

{{% /alert %}}

TSR (Translation/Skalierung/Rotation) werden am häufigsten im 3D-Szenario verwendet. Wir haben eine Klasse `Transform` bereit gestellt, um auf diese in Aspose.3D zuzugreifen. Affine Transformationen umfassen:

- Übersetzung
- Skalierung
- Rotation
- Scher kartierung
- Squeeze-Mapping

{{% alert color="primary" %}}

Das [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](/3d/de/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Drehen Sie durch Quaternion**
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
// Set rotation
cubeNode.Transform.Rotation = Quaternion.FromRotation(new Vector3(0, 1, 0), new Vector3(0.3, 0.5, 0.1));            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **Drehen Sie durch Euler Winkel**
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
// Euler angles
cubeNode.Transform.EulerAngles = new Vector3(0.3, 0.1, -0.5);            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            

// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **Individuelle Transformation matrix**
Wir können Matrix auch direkt verwenden:

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
// Set custom translation matrix
cubeNode.Transform.TransformMatrix = new Matrix4(
1, -0.3, 0, 0,
0.4, 1, 0.3, 0,
0, 0, 1, 0,
0, 20, 0, 1
);        
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
