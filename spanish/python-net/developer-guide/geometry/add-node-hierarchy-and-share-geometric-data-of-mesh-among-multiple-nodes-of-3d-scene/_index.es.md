---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 40
url: /es/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET ofrece la construcción de una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
---
##  **Agregar jerarquía de nodos en el documento de escena 3D**
Aspose.3D for Python via .NET ofrece la construcción de una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
###  **Ejemplo de gráfico de escena**
Se parece a una jerarquía de escena de muestra:

¡! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

En Aspose.3D, cada instancia `Node` puede tener múltiples nodos hijos, en este ejemplo, creamos un nodo con dos nodos de cubo, si rotamos el nodo raíz, todos los nodos hijos también se ven afectados:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
##  **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class puede vincularse a varias instancias de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Supongamos que necesita un sistema en el que todos los 3D cubos parecían ser indistinguibles, sin embargo, requirió una gran cantidad de ellos. Podría ahorrar memoria haciendo un objeto Mesh cuando el sistema se inicie. En ese momento, cada vez que necesite otra forma, crea otro objeto Node y, a continuación, señala ese nodo a la Mesh. Esto se llama instanciación. Aspose.3D for Python via .NET Las APIs permiten hacer instanciación.
###  **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demostración del código de ejemplo:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
