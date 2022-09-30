---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 40
url: /es/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET ofrece construir una jerarquía de nodos. El Nodo es el componente básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al conectar geometrías, luces y cámaras a los nodos.
---
## **Añadir jerarquía de nodos en el documento de escena 3D**
Aspose.3D for .NET ofrece construir una jerarquía de nodos. El Nodo es el componente básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al conectar geometrías, luces y cámaras a los nodos.
### **Ejemplo de gráfico de escena**
Se parece a una jerarquía de escena de muestra:

![Todo: imagen_Alt_Texto](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

En Aspose.3D, cada instancia `Node` puede tener varios nodos secundarios, en este ejemplo, creamos un nodo con dos nodos de cubo, si giramos el nodo raíz, todos los nodos secundarios también se ven afectados:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.cs" >}}
## **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class puede vincularse a varias instancias de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Imagínese que necesita un sistema donde todos los cubos 3D parecieran indistinguibles, sin embargo, requirió numerosos y un gran número de ellos. Puede ahorrar memoria haciendo un objeto Mesh cuando el sistema comienza. En ese momento, cada vez que necesite otra forma, haga otro objeto Node y, a continuación, apunte ese nodo a la Malla. Esto se llama instancing. Aspose.3D for .NET Las API permiten realizar instancias.
### **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demostración del código de ejemplo:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.cs" >}}

En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
