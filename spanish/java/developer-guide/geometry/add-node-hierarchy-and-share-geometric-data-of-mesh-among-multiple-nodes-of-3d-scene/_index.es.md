---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 20
url: /es/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java tiene soporte para construir una jerarquía de nodos. El nodo es un bloque de construcción básico de la escena 3D y una jerarquía de nodos define la estructura lógica de la escena 3D y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
---
##  **Agregar jerarquía de nodos en el documento de escena 3D**
Aspose.3D for Java tiene soporte para construir una jerarquía de nodos. El `Node` es el bloque de construcción básico de la escena 3D y una jerarquía de nodos define la estructura lógica de la escena 3D y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
###  **Ejemplo de gráfico de escena**

En Aspose.3D, cada instancia `Node` puede tener múltiples nodos hijos, en este ejemplo, creamos un nodo con dos nodos de cubo, si rotamos el nodo raíz, todos los nodos hijos también se ven afectados:

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
##  **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de `Mesh` Class puede vincularse a varias instancias de `Node` Class. Supongamos que necesita un sistema en el que todos los 3D cubos parecían ser indistinguibles, sin embargo, requirió una gran cantidad de ellos. Podría ahorrar memoria haciendo un objeto Mesh cuando el sistema se inicie. En ese punto, cada vez que necesite otra forma, crea otro objeto Node, luego apunta ese nodo al `Mesh`. Esto se llama instanciación. Aspose.3D for Java Las API permiten hacer instanciación.
###  **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demostración del código de ejemplo:

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


En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
