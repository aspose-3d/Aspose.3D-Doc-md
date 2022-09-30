---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 20
url: /es/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java tiene soporte para construir una jerarquía de nodos. El nodo es un bloque de construcción básico de la escena 3D y una jerarquía de nodos define la estructura lógica de la escena 3D y proporciona contenido visible al conectar geometrías, luces y cámaras a los nodos.
---
## **Añadir jerarquía de nodos en el documento de escena 3D**
Aspose.3D for Java tiene soporte para construir una jerarquía de nodos. El `Node` es un bloque de construcción básico de la escena 3D y una jerarquía de nodos define la estructura lógica de la escena 3D y proporciona contenido visible al conectar geometrías, luces y cámaras a los nodos.
### **Ejemplo de gráfico de escena**

En Aspose.3D, cada instancia `Node` puede tener varios nodos secundarios, en este ejemplo, creamos un nodo con dos nodos de cubo, si giramos el nodo raíz, todos los nodos secundarios también se ven afectados:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de `Mesh` Class puede vincularse a varias instancias de `Node` Class. Imagínese que necesita un sistema donde todos los cubos 3D parecieran indistinguibles, sin embargo, requirió numerosos y un gran número de ellos. Puede ahorrar memoria haciendo un objeto Mesh cuando el sistema comienza. En ese momento, cada vez que necesite otra forma, haga otro objeto Node y, a continuación, apunte ese nodo al `Mesh`. Esto se llama instancing. Aspose.3D for Java Las API permiten hacer instancing.
### **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}} 

El objeto de clase `Mesh` se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demostración del código de ejemplo:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
