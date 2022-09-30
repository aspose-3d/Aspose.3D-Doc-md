---
title: Configurar normales o UV en el cubo y agregar material a 3D entidades
type: docs
weight: 60
url: /es/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java ofrece gestionar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice, posición en el espacio y su normal, conocido como vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado y debe ser un vector unitario. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2D separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.
---
{{% alert color="primary" %}}

Aspose.3D for Java ofrece gestionar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice, posición en el espacio y su normal, conocido como vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado y debe ser un vector unitario. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2D separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra aquí](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Y, a continuación, seleccione el nodo de la geometría de malla creando una escena 3D.

{{% /alert %}}
## **Crear vectores normales**
Para tener un buen aspecto visual de la iluminación, necesitamos especificar información normal para cada vértice. Para tener los mejores detalles, también podemos usar un mapa normal y difuso (use un mapa de sombra/especular) para realizar un color/normal por píxel. VertexElement logra una información por vértice como el color normal o el vértice. En Aspose.3D podemos mapear información adicional para controlar puntos/vértice de polígono/borde, una muestra para definir normales para el vértice:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
## **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
El Aspose.3D proporciona 5 modos de mapeo:

- **Punto de control**: Cada dato se asigna al punto de control de la geometría.
- **Poligonvértice**-Los datos se asignan al vértice del polígono.
- **Polígono**-Los datos se asignan al polígono.
- **Borde**-Los datos se asignan al borde.
- **AllSame**-Un dato mapeado a toda la geometría.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **Añadir materiales a objetos 3D**
Aspose.3D for Java permite a los desarrolladores utilizar el algoritmo de sombreado para obtener un sombreado y resaltes precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto en el nodo. Rendering Físicamente Basado (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de materiales como en el mundo real.
### **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
### **Aplicar material de rendering basado en la física (PBR) a una caja**
El PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material PBR a 3D objetos en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
