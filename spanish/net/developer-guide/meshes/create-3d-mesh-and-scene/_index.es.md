---
title: Crear 3D Malla y escena
type: docs
weight: 10
url: /es/net/create-3d-mesh-and-scene/
description: Una malla se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. Este artículo explica cómo definir una malla.
---
##  **Crear una malla de cubo 3D**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. Este artículo explica cómo definir un `Mesh`.

Para crear una superficie `Mesh`, necesitamos definir los puntos de control y polígonos de la siguiente manera:

- [Definir los puntos de control](/3d/es/net/create-3d-mesh-and-scene/)
- [Crear polígonos con la clase PolygonBuilder](/3d/es/net/create-3d-mesh-and-scene/)
- [Crear polígonos](/3d/es/net/create-3d-mesh-and-scene/)

Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:
###  **Definir los puntos de control**
Una malla está compuesta por un conjunto de puntos de control en el espacio, y polígonos para describir la superficie de la malla, para crear una malla, necesitamos definir los puntos de control:

{{% alert color="primary" %}}

Los puntos de control de todas las geometrías en Aspose.3D usan coordenadas homogéneas, por lo que es `Vector4` en lugar de Vector3 en el código de ejemplo.

{{% /alert %}}

**Ejemplo:**

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


###  **Crear polígonos**
Los puntos de control no son representables, para hacer visible el cubo, necesitamos definir polígonos en cada lado:

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


###  **Crear polígonos con la clase PolygonBuilder**
También podemos definir polígono por vértices con la clase `PolygonBuilder`:

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

Ahora que está terminado, para hacer visible la malla, necesitamos preparar un nodo para ello.
##  **Cómo triangular una malla**
La malla triangular es útil para la industria de juegos porque la triangular es la única primitiva admitida que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, lo cual es ineficiente en la representación en tiempo real)

{{% alert color="primary" %}}

En esta versión, solo triangulamos los polígonos, ya que es requerido por la exportación de archivos 3ds, las normales/uvs y otros elementos de vértice se pierden durante este procedimiento, podemos implementar esto en el futuro.

{{% /alert %}}

En este ejemplo, triangulamos una malla importando un archivo FBX y lo guardamos en formato FBX.

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
##  **Crear una escena de cubo 3D**
En este tema se muestra cómo añadir geometría Mesh a la escena 3D. El código de ejemplo coloca una escena 3D de cubo y guardado en los formatos de archivo admitidos.
###  **Crear un nodo de cubo**
Un nodo es invisible, pero la geometría unida al nodo se puede renderizar.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Ejemplo**

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

NOTA: Las entidades asociadas al nodo raíz generalmente se ignoran en los softwares CAD/CAM, por lo que necesitamos crear un nuevo nodo para representar la geometría.

{{% /alert %}}
