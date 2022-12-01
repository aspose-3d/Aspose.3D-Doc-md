---
title: Convertir malla a malla de triángulo y forma primitiva a malla
type: docs
weight: 30
url: /es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API permite a los desarrolladores convertir cualquier objeto de malla en malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define mediante la clase Struct o dinámicamente por VertexDeclaration en los ejemplos de código.
---
## **Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API permite a los desarrolladores convertir cualquier objeto de malla en malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado del Vertex se define usando la clase Struct o dinámicamente por [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) en los ejemplos de código.

{{% alert color="primary" %}}

Este tema de ayuda crea mallas del cuadro y la esfera para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda:[Crear una malla de cubo 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Estos ejemplos muestran cómo:

- [Convertir una malla de esfera a triángulo con diseño de memoria personalizado del vértice (definido en la estructura)](/3d/es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertir una malla de caja a triángulo con diseño de memoria personalizado del vértice (definido por la clase VertexDeclaration)](/3d/es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convertir malla**
Los desarrolladores pueden convertir malla en malla triangular porque cualquier estructura compleja (de superficie) se puede representar como un montón de triángulos. El triángulo es la geometría más atómica. Así se utiliza como base para casi cualquier cosa.
### **Acceda a los vértices de una malla triangular**
Los desarrolladores pueden acceder a índices, vértices reales, vértices antes de fusionar y total de bytes de vértices en la memoria.

A continuación, el ejemplo convierte una esfera en una malla triangular con un diseño de memoria personalizado.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.cs" >}}




El siguiente ejemplo convierte una malla Box en triángulo con un diseño de memoria personalizado.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.cs" >}}
## **Convertir la primitiva a una malla**
Usando Aspose.3D for .NET, los desarrolladores pueden convertir cualquier objeto primitivo en una malla. Las primitivas incluyen muchos de los objetos más básicos y más utilizados, como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente una interfaz `IMeshConvertible` se puede convertir en malla mientras se exporta a cualquier formato de archivo 3D.

{{% /alert %}}
### **Convertir una esfera a malla**
Una esfera es un objeto geométrico perfectamente redondo en un espacio tridimensional que aparece en todas partes, desde balones deportivos hasta planetas en el espacio. Usemos la Esfera primitiva para crear una malla.
El ejemplo de código a continuación convierte una esfera en malla.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.cs" >}}
### **Convertir una caja a malla**
Una caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenido. Usemos la caja primitiva para crear una malla. El ejemplo de código a continuación convierte un Box en malla.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.cs" >}}
### **Convertir un avión a malla**
Un plano se extiende infinitamente sin espesor. Un ejemplo de un plano es un plano de coordenadas. Usamos el primitivo `Plane` para crear una malla. El siguiente ejemplo de código convierte un `Plane` a `Mesh`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.cs" >}}
### **Convertir un cilindro a malla**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo, como pilar frente a una casa o como eje de transmisión de automóviles. Permite usar el cilindro primitivo para crear una malla. El ejemplo de código a continuación convierte un cilindro en malla.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.cs" >}}
### **Convertir un torus a malla**
Un toro es una superficie de revolución generada al girar un círculo en un espacio tridimensional alrededor de un eje coplanar con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos el primitivo Torus para crear una malla. El siguiente ejemplo de código convierte un Torus a malla.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.cs" >}}
