---
title: Configurar normales o UV en el cubo y agregar material a entidades 3D
type: docs
weight: 20
url: /es/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Cómo crear datos normales o uv en una malla en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET ofrece administrar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice son su posición en el espacio y su normal, un vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado. Las normales deben ser vectores unitarios. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2d separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos [Crear un objeto de clase `Mesh` como se narra allí](/3d/es/python-net/create-3d-mesh-and-scene/) y luego apuntar el nodo a la geometría de malla por [Creación de una escena 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Crear vectores normales**
Para tener un buen aspecto visual en la iluminación, necesitamos especificar información de normales para cada vértice, para tener mejores detalles, también podemos usar mapa normal y difuso (seguro que puede usar mapa de sombra/especular) para realizar por píxel normal/color. Una información por vértice como el color normal o de vértice se logra mediante `VertexElement`. En Aspose.3D podemos asignar información adicional a los puntos de control/vértice del polígono/borde, una muestra para definir las normales para el vértice:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
##  **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
Aspose.3D proporciona 5 modos de asignación:

- `CONTROL_POINT` -cada dato se asigna al punto de control de la geometría.
- `POLYGON_VERTEX` -los datos se asignan al vértice del polígono.
- `POLYGON` -los datos se asignan al polígono.
- `EDGE` -los datos se asignan al borde.
- `ALL_SAME` -un dato asignado a toda la geometría.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
##  **Agregar materiales a objetos 3D**
Aspose.3D for Python via .NET permite a los desarrolladores utilizar el algoritmo de sombreado para un sombreado y resaltados precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto al nodo. Physically Based Rendering (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de los materiales como en el mundo real.
###  **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
###  **Aplicar material de rendering basado en la física (PBR) a una caja**
PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material de PBR a objetos 3D en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
