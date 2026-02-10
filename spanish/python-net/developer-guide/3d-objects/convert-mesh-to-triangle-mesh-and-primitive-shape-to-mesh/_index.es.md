---
title: Convertir malla a malla de triángulo y forma primitiva a malla
type: docs
weight: 30
url: /es/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Python via .NET API permite a los desarrolladores convertir cualquier objeto de malla a malla triangular con un diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define mediante la clase Struct o dinámicamente por VertexDeclaration en los ejemplos de código.
---
##  **Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice**
[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API permite a los desarrolladores convertir cualquier objeto de malla a malla triangular con un diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define utilizando la clase Struct o dinámicamente por [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) en los ejemplos de código.

{{% alert color="primary" %}}

Este tema de ayuda crea mallas de la caja y la esfera para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](/3d/es/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Estos ejemplos muestran cómo:

- [Convertir una malla de esfera a triángulo con diseño de memoria personalizado del vértice (definido en la estructura)](/3d/es/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertir una malla de caja a triángulo con diseño de memoria personalizado del vértice (definido por la clase VertexDeclaration)](/3d/es/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convertir malla**
Los desarrolladores pueden convertir malla en malla triangular porque cualquier estructura compleja (de superficie) se puede representar como un montón de triángulos. El triángulo es la geometría más atómica. Así se utiliza como base para casi cualquier cosa.
###  **Acceda a los vértices de una malla triangular**
Los desarrolladores pueden acceder a índices, vértices reales, vértices antes de fusionar y total de bytes de vértices en la memoria.

A continuación, el ejemplo convierte una esfera en una malla triangular con un diseño de memoria personalizado.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




El siguiente ejemplo convierte una malla Box en triángulo con un diseño de memoria personalizado.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
##  **Convertir la 'primitiva' a una 'mesa'**
Usando Aspose.3D for Python via .NET, los desarrolladores pueden convertir cualquier objeto primitivo a una malla. Las primitivas incluyen muchos de los objetos más básicos y usados como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente una interfaz IMeshConvertible se puede convertir en malla mientras se exporta a cualquier formato de archivo 3D.

{{% /alert %}}
###  **Convertir una 'Esfera' a 'Mesa'**
Una esfera es un objeto geométrico perfectamente redondo en un espacio tridimensional que aparece en todas partes, desde balones deportivos hasta planetas en el espacio. Usemos la Esfera primitiva para crear una malla.
El ejemplo de código a continuación convierte una esfera en malla.

{{< highlight "python" >}}
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Sphere class
convertible = Sphere()
#  Convert a Sphere to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convertir una 'Box' a 'Mesh'**
Una caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenido. Usemos la caja primitiva para crear una malla. El ejemplo de código a continuación convierte un Box en malla.

{{< highlight "python" >}}
from aspose.threed.entities import Box

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Box class
convertible = Box()
#  Convert a Box to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convertir un 'Plane' a 'Mesh'**
Un plano se extiende infinitamente sin espesor. Un ejemplo de un plano es un plano de coordenadas. Permite utilizar la primitiva Plano para crear una malla. El siguiente ejemplo de código convierte un plano a malla.

{{< highlight "python" >}}
from aspose.threed.entities import Plane

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Plane class
convertible = Plane()
#  Convert a Plane to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convertir un 'Cilindo' a 'Malla'**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo, como pilar frente a una casa o como eje de transmisión de automóviles. Permite usar el cilindro primitivo para crear una malla. El ejemplo de código a continuación convierte un cilindro en malla.

{{< highlight "python" >}}
from aspose.threed.entities import Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Cylinder class
convertible = Cylinder()
#  Convert a Cylinder to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convertir un 'Torus' a 'Mesh'**
Un toro es una superficie de revolución generada al girar un círculo en un espacio tridimensional alrededor de un eje coplanar con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos el primitivo Torus para crear una malla. El siguiente ejemplo de código convierte un Torus a malla.

{{< highlight "python" >}}
from aspose.threed.entities import Torus

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Torus class
convertible = Torus()
#  Convert a Torus to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
