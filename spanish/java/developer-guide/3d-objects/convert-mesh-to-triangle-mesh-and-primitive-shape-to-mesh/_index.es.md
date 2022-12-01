---
title: Convertir malla a malla de triángulo y forma primitiva a malla
type: docs
weight: 20
url: /es/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API tiene soporte para convertir malla en malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado del Vertex se define dinámicamente mediante la clase VertexDeclaration en los ejemplos de código.
---
## **Convertir malla a malla triangular con diseño de memoria personalizado de vértice**
Aspose.3D for Java API tiene soporte para convertir malla en malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado del Vertex se define dinámicamente por la clase `VertexDeclaration` en los ejemplos de código.

{{% alert color="primary" %}}

Este tema de ayuda crea mallas del cuadro y la esfera para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda:[Crear 3D Cubo de malla](/3d/es/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Los desarrolladores pueden convertir malla en malla triangular porque cualquier estructura compleja (de superficie) se puede representar como un montón de triángulos. El triángulo es la geometría más atómica. Así se utiliza como base para casi cualquier cosa. Este ejemplo de código convierte una malla Box en triángulo con diseño de memoria personalizado.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
## **Convertir forma primitiva a malla**
Aspose.3D for Java API tiene el soporte de convertir cualquier forma primitiva en malla. Las formas primitivas incluyen la mayoría de los objetos básicos y utilizados como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente una interfaz ImeshConvertible se puede convertir en malla mientras se exporta a cualquier formato de archivo 3D.

{{% /alert %}}
### **Convertir Esfera primitiva a Malla**
Una esfera es un objeto geométrico perfectamente redondo en un espacio tridimensional que aparece en todas partes, desde balones deportivos hasta planetas en el espacio. Usemos la Esfera primitiva para crear una malla.
El ejemplo de código a continuación convierte una esfera en malla.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
### **Convertir caja a malla**
Una caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenido. Usemos la caja primitiva para crear una malla. El ejemplo de código a continuación convierte un Box en malla.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
### **Convertir un avión a malla**
Un plano se extiende infinitamente sin espesor. Un ejemplo de un plano es un plano de coordenadas. Permite utilizar la primitiva Plano para crear una malla. El siguiente ejemplo de código convierte un plano a malla.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
### **Convertir un cilindro a malla**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo, como pilar frente a una casa o como eje de transmisión de automóviles. Permite usar el cilindro primitivo para crear una malla. El ejemplo de código a continuación convierte un cilindro en malla.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
### **Convertir un torus a malla**
Un toro es una superficie de revolución generada al girar un círculo en un espacio tridimensional alrededor de un eje coplanar con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos el primitivo Torus para crear una malla. El siguiente ejemplo de código convierte un Torus a malla.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
