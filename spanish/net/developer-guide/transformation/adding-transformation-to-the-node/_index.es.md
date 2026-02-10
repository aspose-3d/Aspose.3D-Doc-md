---
title: Adición de transformación al nodo
type: docs
weight: 30
url: /es/net/adding-transformation-to-the-node/
description: TSR (Traducción/Escalado/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase Transform para acceder a estos en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET ofrece rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de objetos en el espacio 3D, ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Traducción/Escalado/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase `Transform` para acceder a estos en Aspose.3D. Las transformaciones afín incluyen:

- Traducción
- Escala
- Rotación
- Mapeo de cizalla
- Mapeo de apretar

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Girar por el cuaternión**
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
##  **Girar por ángulos de Euler**
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
##  **Matriz de transformación personalizada**
También podemos utilizar la matriz directamente:

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
