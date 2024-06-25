---
title: Crear 3D Malla y escena
type: docs
weight: 10
url: /es/python-net/create-3d-mesh-and-scene/
description: Una malla se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. Este artículo explica cómo definir una malla.
---
##  **Crear una malla de cubo 3D**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) se define por un conjunto de puntos de control y los muchos polígonos de n lados según sea necesario. En este artículo se explica cómo definir una malla.

Para crear una superficie de malla, necesitamos definir puntos de control y polígonos de la siguiente manera:

- [Definir los puntos de control](/3d/es/python-net/create-3d-mesh-and-scene/)
- [Crear polígonos con la clase PolygonBuilder](/3d/es/python-net/create-3d-mesh-and-scene/)
- [Crear polígonos](/3d/es/python-net/create-3d-mesh-and-scene/)

Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:
###  **Definir los puntos de control**
Una malla está compuesta por un conjunto de puntos de control en el espacio, y polígonos para describir la superficie de la malla, para crear una malla, necesitamos definir los puntos de control:

{{% alert color="primary" %}}

Los puntos de control de todas las geometrías en Aspose.3D usan coordenadas homogéneas, por lo que es `Vector4` en lugar de `Vector3` en el código de ejemplo.

{{% /alert %}}

**Ejemplo:**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-DefineControlPoints.py" >}}


###  **Crear polígonos**
Los puntos de control no son representables, para hacer visible el cubo, necesitamos definir polígonos en cada lado:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.py" >}}


###  **Crear polígonos con la clase PolygonBuilder**
También podemos definir polígono por vértices con la clase `PolygonBuilder`:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.py" >}}

Ahora que está terminado, para hacer visible la malla, necesitamos preparar un nodo para ello.
##  **Cómo triangular una malla**
La malla triangular es útil para la industria de juegos porque la triangular es la única primitiva admitida que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, lo cual es ineficiente en la representación en tiempo real)

{{% alert color="primary" %}}

En esta versión, solo triangulamos los polígonos, ya que es requerido por la exportación de archivos 3ds, las normales/uvs y otros elementos de vértice se pierden durante este procedimiento, podemos implementar esto en el futuro.

{{% /alert %}}

En este ejemplo, triangulamos una malla importando un archivo FBX y lo guardamos en formato FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Crear una escena de cubo 3D**
En este tema se muestra cómo añadir geometría Mesh a la escena 3D. El código de ejemplo coloca una escena 3D de cubo y guardado en los formatos de archivo admitidos.
###  **Crear un nodo de cubo**
Un nodo es invisible, pero la geometría unida al nodo se puede renderizar.

{{% alert color="primary" %}}

The Mesh class object is being used in the code. We can [create a `Mesh` class object as narrated there](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Ejemplo**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-CubeScene-CreateCubeScene.py" >}}

{{% alert color="primary" %}}

NOTA: Las entidades asociadas al nodo raíz generalmente se ignoran en los softwares CAD/CAM, por lo que necesitamos crear un nuevo nodo para representar la geometría.

{{% /alert %}}
