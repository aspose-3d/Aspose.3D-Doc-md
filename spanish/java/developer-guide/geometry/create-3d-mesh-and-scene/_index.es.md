---
title: Crear 3D Malla y escena
type: docs
weight: 40
url: /es/java/create-3d-mesh-and-scene/
description: Una malla se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. Este artículo explica cómo definir una malla.
---
##  **Crear una malla de cubo 3D**
A `Mesh` se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. Este artículo explica cómo definir un `Mesh`.

Para crear una superficie `Mesh`, necesitamos definir los puntos de control y polígonos de la siguiente manera:

- [Definir los puntos de control](/3d/es/java/create-3d-mesh-and-scene-html/)
- [Crear polígonos con la clase PolygonBuilder](/3d/es/java/create-3d-mesh-and-scene-html/)
- [Crear polígonos](/3d/es/java/create-3d-mesh-and-scene-html/)

Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:
###  **Definir los puntos de control**
Una malla está compuesta por un conjunto de puntos de control en el espacio, y polígonos para describir la superficie de la malla, para crear una malla, necesitamos definir los puntos de control:

{{% alert color="primary" %}} 

Los puntos de control de todas las geometrías en Aspose.3D usan coordenadas homogéneas, por lo que es `Vector4` en lugar de `Vector3` en el código de ejemplo.

{{% /alert %}} 

**Ejemplo:**

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



###  **Crear polígonos**
Los puntos de control no son representables, para hacer visible el cubo, necesitamos definir polígonos en cada lado:

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



###  **Crear polígonos con la clase PolygonBuilder**
También podemos definir polígono por vértices con la clase PolygonBuilder:

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

Ahora que está terminado, para hacer visible la malla, necesitamos preparar un nodo para ello.
##  **Cómo triangular una malla**
La malla triangular es útil para la industria de juegos porque la triangular es la única primitiva admitida que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, lo cual es ineficiente en la representación en tiempo real)

{{% alert color="primary" %}} 

En esta versión, solo triangulamos los polígonos, ya que es requerido por la exportación de archivos 3ds, las normales/uvs y otros elementos de vértice se pierden durante este procedimiento, podemos implementar esto en el futuro.

{{% /alert %}} 

En este ejemplo, triangulamos una malla importando un archivo FBX y lo guardamos en formato FBX.

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
##  **Crear una escena de cubo 3D**
En este tema se muestra cómo añadir geometría Mesh a la escena 3D. El código de ejemplo coloca una escena 3D de cubo y guardado en los formatos de archivo admitidos.
###  **Crear un nodo de cubo**
Un nodo es invisible, pero la geometría unida al nodo se puede renderizar.

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Ejemplo:**

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

NOTA: Las entidades asociadas al nodo raíz generalmente se ignoran en los softwares CAD/CAM, por lo que necesitamos crear un nuevo nodo para representar la geometría.

{{% /alert %}}
