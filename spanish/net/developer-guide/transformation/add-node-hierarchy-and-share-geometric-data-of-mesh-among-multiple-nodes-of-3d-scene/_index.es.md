---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 40
url: /es/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET ofrece construir una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
---
##  **Agregar jerarquía de nodos en el documento de escena 3D**
Aspose.3D for .NET ofrece construir una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
###  **Ejemplo de gráfico de escena**
Se parece a una jerarquía de escena de muestra:

¡! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

En Aspose.3D, cada instancia `Node` puede tener múltiples nodos hijos, en este ejemplo, creamos un nodo con dos nodos de cubo, si rotamos el nodo raíz, todos los nodos hijos también se ven afectados:

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
##  **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class puede vincularse a varias instancias de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Supongamos que necesita un sistema en el que todos los 3D cubos parecían ser indistinguibles, sin embargo, requirió una gran cantidad de ellos. Podría ahorrar memoria haciendo un objeto Mesh cuando el sistema se inicie. En ese momento, cada vez que necesite otra forma, crea otro objeto Node y, a continuación, señala ese nodo a la Mesh. Esto se llama instanciación. Aspose.3D for .NET Las API permiten hacer instanciación.
###  **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demostración del código de ejemplo:

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

En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
