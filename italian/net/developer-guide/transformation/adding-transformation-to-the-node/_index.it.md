---
title: Aggiunta della trasformazione al nodo
type: docs
weight: 30
url: /it/net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe Transform per accedere a questi in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET offre la possibilità di ruotare gli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Traduzione/Scaling/Rotazione) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe `Transform` per accedere a questi in Aspose.3D. Le trasformazioni affini includono:

- Traduzione
- Scalatura
- Rotazione
- Mappatura del taglio
- Spremi la mappatura

{{% alert color="primary" %}}

L'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Ruota da Quaternion**
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
##  **Ruota per angoli di Eulero**
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
##  **Matrice di trasformazione personalizzata**
Possiamo anche usare Matrix direttamente:

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
