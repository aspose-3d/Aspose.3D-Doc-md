---
title: Configurar normales o UV en el cubo y añadir material a 3D Entidades
type: docs
weight: 20
url: /es/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Cómo crear datos normales o uv en una malla en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET ofrece gestionar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice son su posición en el espacio y su normal, un vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado. Las normales deben ser vectores unitarios. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2d separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-3d-mesh-and-scene/)Y, a continuación, apunte el nodo a la geometría de malla por[Creación de una escena 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Crear vectores normales**
Para tener un buen aspecto visual en la iluminación, necesitamos especificar la información normal para cada vértice, para tener mejores detalles, también podemos usar el mapa normal y difuso (seguro que puede usar la sombra/mapa especular) para realizar por píxel normal/color. VertexElement logra una información por vértice como el color normal o el vértice. En Aspose.3D podemos mapear información adicional para controlar puntos/vértice de polígono/borde, una muestra para definir normales para el vértice:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.cs" >}}

Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
## **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
El Aspose.3D proporciona 5 modos de mapeo:

- `ControlPoint`: cada dato se asigna al punto de control de la geometría.
- `PolygonVertex`: los datos se asignan al vértice del polígono.
- `Polygon`: los datos se asignan al polígono.
- `Edge`: los datos se asignan al borde.
- `AllSame`: un dato asignado a toda la geometría.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.cs" >}}
## **Añadir materiales a objetos 3D**
Aspose.3D for .NET permite a los desarrolladores utilizar el algoritmo de sombreado para obtener un sombreado y resaltes precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto en el nodo. Rendering Físicamente Basado (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de materiales como en el mundo real.
### **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.cs" >}}

Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
### **Aplicar material de rendering basado en la física (PBR) a una caja**
El PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material PBR a 3D objetos en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
